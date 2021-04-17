---
title: Estructura de _VIDEOINFOHEADER
description: La \_ estructura VIDEOINFOHEADER contiene información sobre un flujo de vídeo e incluye una \_ estructura BITMAPINFOHEADER que define el formato de un fotograma individual.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Estructura _VIDEOINFOHEADER Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698533"
---
# <a name="_videoinfoheader-structure"></a>\_Estructura VIDEOINFOHEADER

La estructura **\_ VIDEOINFOHEADER** contiene información sobre un flujo de vídeo e incluye una estructura **\_ BITMAPINFOHEADER** que define el formato de un fotograma individual.

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

Estructura **Rect** que especifica la ventana de vídeo de origen.

</dd> <dt>

**rcTarget**
</dt> <dd>

Estructura **Rect** que especifica la ventana de vídeo de destino.

</dd> <dt>

**dwBitRate**
</dt> <dd>

Valor **DWORD** que especifica la velocidad de datos aproximada del flujo de vídeo, en bits por segundo.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

Valor **DWORD** que especifica la tasa de errores de datos de la secuencia de vídeo, en errores de bits por segundo.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**Referencia \_ de** Valor de tiempo que especifica el promedio de tiempo de visualización del fotograma de vídeo, en unidades de 100-nanosegundos.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Estructura **\_ BITMAPINFOHEADER** de Win32 que contiene información de color y dimensión para el mapa de bits de imagen de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





