---
title: _VIDEOINFOHEADER estructura
description: La estructura VIDEOINFOHEADER contiene información sobre una secuencia de vídeo e incluye una estructura BITMAPINFOHEADER que define el \_ formato de un fotograma \_ individual.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER estructura windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b00c641f0fb9a9f68217de8a21a732b4b45a8e4417104be981ffd90161f7340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586805"
---
# <a name="_videoinfoheader-structure"></a>\_Estructura VIDEOINFOHEADER

La **\_ estructura VIDEOINFOHEADER** contiene información sobre una secuencia de vídeo e incluye una estructura **\_ BITMAPINFOHEADER** que define el formato de un fotograma individual.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**rcSource**
</dt> <dd>

**Estructura RECT** que especifica la ventana de vídeo de origen.

</dd> <dt>

**rcTarget**
</dt> <dd>

**Estructura RECT** que especifica la ventana de vídeo de destino.

</dd> <dt>

**dwBitRate**
</dt> <dd>

**Valor DWORD** que especifica la velocidad de datos aproximada de la secuencia de vídeo, en bits por segundo.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

**Valor DWORD** que especifica la tasa de errores de datos de la secuencia de vídeo, en errores de bits por segundo.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**REFERENCIA \_ Valor** TIME que especifica el tiempo medio de visualización del fotograma de vídeo, en unidades de 100 nanosegundos.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Estructura **\_ BITMAPINFOHEADER** de Win32 que contiene información de color y dimensión para el mapa de bits de imagen de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





