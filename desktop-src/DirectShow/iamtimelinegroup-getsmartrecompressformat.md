---
description: El método GetSmartRecompressFormat recupera el formato de compresión actual para la recompresión inteligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: Método IAMTimelineGroup::GetSmartRecompressFormat (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892092"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>Método IAMTimelineGroup::GetSmartRecompressFormat

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetSmartRecompressFormat` método recupera el formato de compresión actual para la recompresión inteligente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFormat* 
</dt> <dd>

Recibe un puntero a una [**estructura SCompFmt0,**](scompfmt0.md) que se convierte como un puntero a un objeto long. Si se produce un error en el método , el valor se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si la aplicación no ha establecido un formato de compresión inteligente (llamando a [**IAMTimelineGroup::SetSmartRecompressFormat),**](iamtimelinegroup-setsmartrecompressformat.md)el formato devuelto por este método no será válido. Llame al [**método IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) para determinar si se estableció un formato de compresión.

Si el método se realiza correctamente, el autor de la llamada debe liberar el tipo de medio devuelto y eliminar la [**estructura SCompFmt0:**](scompfmt0.md)


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



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

[**IAMTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




