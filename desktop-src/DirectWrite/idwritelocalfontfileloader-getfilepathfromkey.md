---
title: Método IDWriteLocalFontFileLoader GetFilePathFromKey
description: Obtiene la ruta de acceso absoluta del archivo de fuente de la clave de referencia del archivo de fuente.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Escritura directa del método GetFilePathFromKey
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
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169869"
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



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





