---
title: IWMPLibraryServices getLibraryByType, método
description: El método getLibraryByType devuelve una interfaz IWMPLibrary que representa la biblioteca que tiene el tipo y el índice especificados.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- método getLibraryByType de Windows Media Player
- método getLibraryByType Windows Media Player, interfaz IWMPLibraryServices
- Interfaz IWMPLibraryServices Windows Media Player, método getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671593"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>IWMPLibraryServices:: getLibraryByType (método)

El método **getLibraryByType** devuelve una interfaz **IWMPLibrary** que representa la biblioteca que tiene el tipo y el índice especificados.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*wmplt* \[ de\]
</dt> <dd>

Un valor de la enumeración **WMPLib. WMPLibraryType** que especifica el tipo de biblioteca que se va a recuperar.

</dd> <dt>

*lIndex* \[ de\]
</dt> <dd>

**System. Int32** que es el índice de la biblioteca que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPLibrary** para la biblioteca que se devuelve.

## <a name="remarks"></a>Observaciones

Solo hay una biblioteca local y las bibliotecas de discos solo están disponibles en CDs de datos y DVDs que contienen contenido multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPLibrary (VB y C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





