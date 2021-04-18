---
title: IWMPCdromBurn getItemInfo, método
description: El método getItemInfo recupera el valor del atributo especificado para el CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718831"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>IWMPCdromBurn:: getItemInfo (método)

El método **getItemInfo** recupera el valor del atributo especificado para el CD.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItem* \[ de\]
</dt> <dd>

**System. String** que contiene uno de los valores siguientes.



| Value         | Descripción                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| AvailableTime | Recupera la hora disponible en el CD, en segundos.                                          |
| En blanco         | Recupera un **System. Boolean** (representado como una cadena) que indica si el CD está en blanco. |
| FreeSpace     | Recupera el espacio disponible en el CD, en bytes.                                                |
| TotalSpace    | Recupera el espacio total en el CD, en bytes.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. String** que es el valor del atributo especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





