---
description: El método get MediaType devuelve el tipo de medio de salida actual del \_ filtro de cambio de tamaño.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: Método IResize::get_MediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d9e23c78a25f1cda141cb0c3ce55688c12bdf3aab447aca596326e01544b4e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818236"
---
# <a name="iresizeget_mediatype-method"></a>IResize::get \_ MediaType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método devuelve el tipo de medio de salida actual del `get_MediaType` filtro de cambio de tamaño.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmt* \[ out\]
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) asignada por el autor de la llamada. El método rellena esta estructura con el tipo de medio. El autor de la llamada debe liberar el bloque de formato, si lo hubiera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Si no se ha establecido el tipo de medio de salida, devuelva un tipo de medio predeterminado. El filtro debe actualizar su tipo de medio de salida cuando se llama a los métodos **\_ put MediaType** o **put \_ Size;** el tipo de medio devuelto por `get_MediaType` debe reflejar estos cambios.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**IResize (Interfaz)**](iresize.md)
</dt> </dl>

 

 




