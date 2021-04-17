---
title: IDWriteLocalFontFileLoader GetFilePathLengthFromKey, método
description: Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Método GetFilePathLengthFromKey de escritura directa
- Método GetFilePathLengthFromKey de escritura directa, interfaz IDWriteLocalFontFileLoader
- Interfaz IDWriteLocalFontFileLoader Direct Write, método GetFilePathLengthFromKey
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
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671206"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>IDWriteLocalFontFileLoader:: GetFilePathLengthFromKey (método)

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

*fontFileReferenceKey* \[ de\]
</dt> <dd>

Tipo: **const void \***

Clave de referencia del archivo de fuente que identifica de forma única el archivo de fuente local dentro del ámbito del cargador de fuentes que se está usando.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

Tamaño de la clave de referencia del archivo de fuentes en bytes.

</dd> <dt>

*filePathLength* \[ enuncia\]
</dt> <dd>

Tipo: **UINT32 \***

Longitud de la cadena de ruta de acceso del archivo, sin incluir el carácter **nulo** terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





