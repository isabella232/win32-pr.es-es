---
title: Método IWMPLibraryServices getLibraryByType
description: El método getLibraryByType devuelve una interfaz IWMPLibrary que representa la biblioteca que tiene el tipo y el índice especificados.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Método getLibraryByType Reproductor de Windows Media
- Método getLibraryByType Reproductor de Windows Media , interfaz IWMPLibraryServices
- Interfaz IWMPLibraryServices Reproductor de Windows Media método , getLibraryByType
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474561"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>IWMPLibraryServices::getLibraryByType (método)

El **método getLibraryByType** devuelve una **interfaz IWMPLibrary** que representa la biblioteca que tiene el tipo y el índice especificados.

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

*wmplt* \[ En\]
</dt> <dd>

Valor de la **enumeración WMPLib.WMPLibraryType** que especifica el tipo de biblioteca que se debe recuperar.

</dd> <dt>

*lIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de la biblioteca que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPLibrary** para la biblioteca que se devuelve.

## <a name="remarks"></a>Observaciones

Solo hay una biblioteca local y las bibliotecas de discos solo están disponibles en LOS CD y DVD de datos que contienen contenido multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
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

 

 





