---
description: El método GetMediaType recupera el tipo de medio sin comprimir para el grupo.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: Método IAMTimelineGroup::GetMediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887017"
---
# <a name="iamtimelinegroupgetmediatype-method"></a>IamTimelineGroup::GetMediaType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetMediaType` método recupera el tipo de medio sin comprimir para el grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmt* \[ out\]
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se rellena con el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El autor de la llamada debe liberar el bloque de formato del tipo de medio devuelto, dado en el **miembro pbFormat** de la estructura AM \_ MEDIA TYPE \_ devuelta. Puede usar la función auxiliar [**FreeMediaType de**](freemediatype.md) la biblioteca de clases base.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




