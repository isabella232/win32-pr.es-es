---
description: El método GetSmartRecompressFormat recupera el formato de compresión actual para la recompresión inteligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'IAMTimelineGroup:: GetSmartRecompressFormat (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690485"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>IAMTimelineGroup:: GetSmartRecompressFormat (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

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

Recibe un puntero a una estructura [**SCompFmt0**](scompfmt0.md) , convertido en un puntero a un valor Long. Si se produce un error en el método, el valor se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si la aplicación no ha establecido un formato de compresión inteligente (llamando a [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), el formato devuelto por este método no será válido. Llame al método [**IAMTimelineGroup:: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) para determinar si se ha establecido un formato de compresión.

Si el método se ejecuta correctamente, el llamador debe liberar el tipo de medio devuelto y eliminar la estructura [**SCompFmt0**](scompfmt0.md) :


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




