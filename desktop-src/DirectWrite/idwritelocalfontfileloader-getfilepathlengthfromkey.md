---
title: Método IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Método GetFilePathLengthFromKey de escritura directa
- Método GetFilePathLengthFromKey direct write , interfaz IDWriteLocalFontFileLoader
- IdWriteLocalFontFileLoader interface Direct Write , GetFilePathLengthFromKey (método GetFilePathLengthFromKey)
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587f432f006493097ec8262fcc2201e2c3b67abe7115c395332671ec35efeba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816356"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>Método IDWriteLocalFontFileLoader::GetFilePathLengthFromKey

Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
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

*filePathLength* \[ out\]
</dt> <dd>

Tipo: **UINT32 \***

Longitud de la cadena de ruta de acceso del archivo, sin incluir el carácter **NULL** terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





