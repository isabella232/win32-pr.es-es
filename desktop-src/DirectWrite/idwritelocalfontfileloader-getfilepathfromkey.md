---
title: Método IDWriteLocalFontFileLoader GetFilePathFromKey
description: Obtiene la ruta de acceso absoluta del archivo de fuente de la clave de referencia del archivo de fuente.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Método GetFilePathFromKey Direct Write
- Método GetFilePathFromKey direct write , interfaz IDWriteLocalFontFileLoader
- IdWriteLocalFontFileLoader interface Direct Write , Método GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7739cfa4a03abb3506bd63a84e0c747021110198f7d0ffefa69116656cbfa616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928035"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Método IDWriteLocalFontFileLoader::GetFilePathFromKey

Obtiene la ruta de acceso absoluta del archivo de fuente de la clave de referencia del archivo de fuente.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fontFileReferenceKey* \[ En\]
</dt> <dd>

Tipo: **const \* void**

Clave de referencia del archivo de fuente que identifica de forma única el archivo de fuente local dentro del ámbito del cargador de fuentes que se está utilizando.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

Tamaño de la clave de referencia del archivo de fuente en bytes.

</dd> <dt>

*filePath* \[ out\]
</dt> <dd>

Tipo: **WCHAR \***

Matriz de caracteres que recibe la ruta de acceso del archivo local.

</dd> <dt>

*filePathSize* 
</dt> <dd>

Tipo: **UINT32**

Longitud de la matriz de caracteres de ruta de acceso de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





