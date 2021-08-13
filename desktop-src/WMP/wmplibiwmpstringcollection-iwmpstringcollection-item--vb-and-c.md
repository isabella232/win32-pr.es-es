---
title: Método IWMPStringCollection Item
description: El método Item devuelve la cadena en el índice especificado.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Método de elemento Reproductor de Windows Media
- Método item Reproductor de Windows Media , interfaz IWMPStringCollection
- Interfaz IWMPStringCollection Reproductor de Windows Media , Método Item
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
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568441"
---
# <a name="iwmpstringcollectionitem-method"></a>IWMPStringCollection::Item (Método)

El **método Item** devuelve la cadena en el índice especificado.

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

*lIndex* \[ En\]
</dt> <dd>

**System.Int32** que es el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es la cadena en el índice especificado.

## <a name="remarks"></a>Observaciones

La **interfaz IWMPStringCollection** se usa para recuperar el conjunto de valores disponibles para un atributo. Por ejemplo, el método **IWMPMediaCollection.getAttributeStringCollection** se puede usar para recuperar una **interfaz IWMPStringCollection** que representa todos los valores del atributo Genre dentro del tipo de medio Audio. A **continuación,** el método Item se puede usar para recorrer en iteración todos los valores posibles para el atributo Genre.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPMediaCollection.getAttributeStringCollection (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





