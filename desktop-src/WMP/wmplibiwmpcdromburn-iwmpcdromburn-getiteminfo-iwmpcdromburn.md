---
title: Método IWMPCdromAsync getItemInfo
description: El método getItemInfo recupera el valor del atributo especificado para el CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , interfaz IWMPCdromAsync
- Interfaz IWMPCdromAsync Reproductor de Windows Media , método getItemInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569017"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>IWMPCdromAsync::getItemInfo (método)

El **método getItemInfo** recupera el valor del atributo especificado para el CD.

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

*bstrItem* \[ En\]
</dt> <dd>

**System.String que** contiene uno de los valores siguientes.



| Value         | Descripción                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| AvailableTime | Recupera el tiempo disponible en el CD, en segundos.                                          |
| En blanco         | Recupera un **objeto System.Boolean** (representado como una cadena) que indica si el CD está en blanco. |
| FreeSpace     | Recupera el espacio libre en el CD, en bytes.                                                |
| TotalSpace    | Recupera el espacio total en el CD, en bytes.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el valor del atributo especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





