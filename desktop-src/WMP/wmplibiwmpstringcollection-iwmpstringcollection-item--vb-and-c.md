---
title: IWMPStringCollection (método del elemento)
description: El método Item devuelve la cadena en el índice especificado.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Método de elemento Media Player de Windows
- Método de elemento Windows Media Player, interfaz IWMPStringCollection
- Interfaz IWMPStringCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708779"
---
# <a name="iwmpstringcollectionitem-method"></a>IWMPStringCollection:: Item (método)

El método **Item** devuelve la cadena en el índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* \[ de\]
</dt> <dd>

**System. Int32** que es el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. String** que es la cadena que se encuentra en el índice especificado.

## <a name="remarks"></a>Observaciones

La interfaz **IWMPStringCollection** se usa para recuperar el conjunto de valores disponibles para un atributo. Por ejemplo, el método **IWMPMediaCollection. getAttributeStringCollection** se puede usar para recuperar una interfaz **IWMPStringCollection** que representa todos los valores del atributo Genre en el tipo de medio de audio. El método **Item** se puede usar para recorrer en iteración todos los valores posibles del atributo Genre.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPMediaCollection. getAttributeStringCollection (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





