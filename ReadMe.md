# React Native Picker

```
import React, { Component } from 'react'
import {
  Text,
  View,
  StyleSheet,
  Picker
} from 'react-native';

class Home extends Component {
  state = {
    namaTempat: '',
  }

  render() {
    return (
        <View style={{flex:1}}>
        <Text style={{ fontSize: 10, textAlign: 'center' }}>Lokasi Anda</Text>
        <Text style={{ fontSize: 6, textAlign: 'center' }}>{this.state.namaTempat}</Text>

        <View style={{ flexDirection: 'row', justifyContent: 'center' }}>
          <Picker
            selectedValue={this.state.namaTempat}
            onValueChange={(itemValue) => this.setState({ namaTempat: itemValue })}
            style={{ width: '80%', color: '#000', fontWeight: 'bold' }}
            mode='dropdown'>
            <Picker.Item label="Cari Lokasi Anda" />
            <Picker.Item label='Kabupaten Bantul' value='Bantul' />
            <Picker.Item label='Kabupaten Gunung Kidul	' value='GunungKidul' />
            <Picker.Item label='Kabupaten Kulon Progo' value='KulonProgo' />
            <Picker.Item label='Kabupaten Sleman' value='Sleman' />
            <Picker.Item label='Kota Yogyakarta' value='Yogyakarta' />
          </Picker>
         </View>
         </View>
    );
  }
}
export default Home;
```
