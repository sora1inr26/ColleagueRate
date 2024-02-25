<template>
    <div class="list">
      <ul>
        <li v-for="item in data" :key="item.id">
          <div class="item">
            <div class="name">{{ item.name }}</div>
            <div class="employees">{{ item.employees }}</div>
            <div class="pk">
              <progress :value="item.pk.like" max="100" class="like"></progress>
              <progress :value="item.pk.dislike" max="100" class="dislike"></progress>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data () {
      return {
        data: [
          {
            id: 1,
            name: '公司 A',
            employees: 100,
            pk: {
              like: 50,
              dislike: 50
            }
          },
          {
            id: 2,
            name: '公司 B',
            employees: 200,
            pk: {
              like: 60,
              dislike: 40
            }
          },
          {
            id: 3,
            name: '公司 C',
            employees: 300,
            pk: {
              like: 70,
              dislike: 30
            }
          }
        ]
      }
    }
  }
  </script>
  
  <style>
  .list {
    width: 100%;
    display: flex;
    flex-direction: column;
  }
  
  .list ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .list li {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    border: 1px solid #ddd;
    padding: 8px;
  }
  
  .list .item {
    width: 100%;
    display: flex;
    align-items: center;
  }
  
  .list .name {
    font-size: 16px;
    font-weight: bold;
    margin-right: 8px;
  }
  
  .list .employees {
    margin-right: 8px;
  }
  
  .list .pk {
    display: flex;
    align-items: center;
  }
  
  .list .progress {
    width: 50%;
    margin-right: 4px;
  }
  
  .like {
    background-color: red;
  }
  
  .dislike {
    background-color: blue;
  }
  
  .dashed {
    border-style: dashed;
  }
  </style>
  