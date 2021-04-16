---
title: IDWriteLocalFontFileLoader GetLastWriteTimeFromKey, método
description: Obtiene la hora de la última escritura del archivo a partir de la clave de referencia del archivo de fuente.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Método GetLastWriteTimeFromKey de escritura directa
- Método GetLastWriteTimeFromKey de escritura directa, interfaz IDWriteLocalFontFileLoader
- Interfaz IDWriteLocalFontFileLoader Direct Write, método GetLastWriteTimeFromKey
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690603"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>IDWriteLocalFontFileLoader:: GetLastWriteTimeFromKey (método)

Obtiene la hora de la última escritura del archivo a partir de la clave de referencia del archivo de fuente.

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

*fontFileReferenceKey* \[ de\]
</dt> <dd>

Tipo: **const void \***

Clave de referencia del archivo de fuente que identifica de forma única el archivo de fuente local dentro del ámbito del cargador de fuentes que se utiliza.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

Tamaño de la clave de referencia del archivo de fuentes en bytes.

</dd> <dt>

*lastWriteTime* \[ enuncia\]
</dt> <dd>

Tipo: **FILETIME \***

Hora de la última modificación del archivo de fuentes.

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

 

 





