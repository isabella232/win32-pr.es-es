---
title: Método IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Obtiene la última hora de escritura del archivo a partir de la clave de referencia del archivo de fuente.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Método GetLastWriteTimeFromKey direct write
- Método GetLastWriteTimeFromKey direct write , interfaz IDWriteLocalFontFileLoader
- Método GetLastWriteTimeFromKey de la interfaz IDWriteLocalFontFileLoader
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169861"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Método IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey

Obtiene la última hora de escritura del archivo a partir de la clave de referencia del archivo de fuente.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
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

*lastWriteTime* \[ out\]
</dt> <dd>

Tipo: **FILETIME \***

Hora de la última modificación del archivo de fuente.

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

 

 





