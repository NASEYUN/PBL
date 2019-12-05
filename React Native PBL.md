# React Native를 이용하여 쇼핑몰 앱 개발하기

### FlatList를 사용하여 쇼핑몰 카테고리를 구현하였다.
### data에 이름, 가격, 이미지를 저장하여 _renderItem으로 item을 가져와서 뷰를 구현하였다.

---

import React, {Component} from 'react';
import { View, FlatList, StyleSheet, Text, Image } from 'react-native';
import Constants from 'expo-constants';

class SimpleList extends Component {

  constructor(props){
    super(props);
    this.state = {
      data : [
  {
    id: 'bd7acbea-c1b1-46c2-aed5-3ad53abb28ba',
    key: 'First Item',
    price: '5000',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQEDAd7-CHpKlNY_DZyfxKrwcKhuzSmnHBhmuTDqzQwcyKbIDSThQ&s'
  },
  {
    id: '3ac68afc-c605-48d3-a4f8-fbd91aa97f63',
    key: 'Second Item',
    price: '10000',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQU64yxCOPyBfUIhPSKacUOWYmrndEniH8hjehHzOHH_lKaJnyD&s'
  },
  {
    id: '58694a0f-3da1-471f-bd96-145571e29d72',
    key: 'Third Item',
    price: '15000',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4q4zOt5beA3ekc1DT8z-LbUtRrsSrwAWzPgKv9PnpQ7OlijfIDQ&s'
  },
  {
    id: '58694a0f-3da1-471f-bd96-145571e29d72',
    key: 'Fourth Item',
    price: '40000',
    image: 'https://simage-kr.uniqlo.com/goods/31/11/38/70/409337_COL_COL36_1000.jpg'
  }
]
}
}


_renderItem = ({item}) => {
  return (
  <View >
    <Image source={{uri:item.image}} style={{
    
      resizeMode:"contain", width:400, height:400}}></Image>
    <Text style={styles.row}>{item.key}</Text> 
    <Text style={styles.row}>{item.price}</Text>
  </View>)
};

render(){
  return (
    <View styles={styles.container}>
      <FlatList 
        data={this.state.data}
        renderItem={this._renderItem}
        />
    </View>
  );
}
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    marginTop: Constants.statusBarHeight,
  },
  row: {
    textAlign:"center"
  }
});

export default SimpleList;
