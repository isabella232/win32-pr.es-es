---
title: Estructura de _WAVEFORMATEX
description: La estructura \_WAVEFORMATEX define el formato de datos de audio Waveform.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Estructura _WAVEFORMATEX Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699519"
---
# <a name="_waveformatex-structure"></a>\_WAVEFORMATEX (estructura)

La estructura **\_ WAVEFORMATEX** define el formato de los datos de audio de forma de onda.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wFormatTag**
</dt> <dd>

Debe establecerse en un formato o en los formatos admitidos por el dispositivo. Tenga en cuenta que en las versiones anteriores de Windows Media Administrador de dispositivos recomendamos usar \_ All Wave Format de WMDM \_ \_ para indicar la compatibilidad con todos los formatos. Sin embargo, esto ya no se recomienda, ya que los distintos reproductores multimedia interpretarán esto de maneras diferentes y algunos dispositivos pueden reproducir realmente cualquier formato de archivo. Ahora se recomienda usar la enumeración de WMDM \_ \_ \_ valores válidos \_ de valores válidos \_ cualquier valor de la enumeración del formulario de enumeración de [**WMDM \_ propiedades de \_ \_ \_ valores \_ válidos**](wmdm-enum-prop-valid-values-form.md) , o bien especificar mejor un intervalo de formatos con la estructura de intervalo de valores de prop de [**WMDM \_ \_ \_**](wmdm-prop-values-range.md) .

</dd> <dt>

**nChannels**
</dt> <dd>

Número de canales en los datos de audio de onda. Los datos monoaural usan un canal y los datos estéreo usan dos canales.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Frecuencia de muestreo, en muestras por segundo (hercios), en la que se debe reproducir o grabar cada canal. Los valores comunes para **nSamplesPerSec** son 8,0 kilohercios (kHz), 11,025 khz, 22,05 khz y 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Velocidad de transferencia de datos media requerida para la etiqueta de formato, en bytes por segundo. El software de reproducción y grabación puede calcular los tamaños de búfer mediante el miembro **nAvgBytesPerSec** .

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Alineación de bloque, en bytes. La alineación de bloque es la unidad atómica mínima de datos para el tipo de formato **wFormatTag** . El software de reproducción y grabación debe procesar un múltiplo de **nBlockAlign** bytes de datos a la vez. Los datos escritos y leídos de un dispositivo siempre deben empezar al principio de un bloque. Por ejemplo, no es posible empezar a reproducir correctamente los datos PCM en medio de un ejemplo (es decir, en un límite que no está alineado con un bloque).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por muestra para el tipo de formato **wFormatTag** .

</dd> <dt>

**cbSize**
</dt> <dd>

Este miembro se omite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





