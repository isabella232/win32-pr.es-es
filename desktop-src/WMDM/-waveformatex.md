---
title: _WAVEFORMATEX estructura
description: La estructura \_WAVEFORMATEX define el formato de datos de audio Waveform.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX estructura windows Media Administrador de dispositivos
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
ms.openlocfilehash: e149608d740df6df40b39b64b09ac11837a721b5b4844f1a73eb52e1b5cea479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586750"
---
# <a name="_waveformatex-structure"></a>\_STRUCTUREATEX (estructura)

La **\_ estructura DESATEX** define el formato de los datos de audio de forma de onda.

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

Debe establecerse en un formato o formatos admitidos por el dispositivo. Tenga en cuenta que las versiones anteriores de Windows Media Administrador de dispositivos se recomienda usar WMDM WAVE FORMAT ALL para indicar la compatibilidad \_ \_ con todos los \_ formatos. Sin embargo, esto ya no se recomienda, ya que los distintos reproductores multimedia lo interpretarán de maneras diferentes y pocos dispositivos pueden reproducir realmente cualquier formato de archivo. Ahora se recomienda usar el valor DE WMDM ENUM PROP VALID VALUES ANY de la enumeración \_ \_ \_ \_ \_ [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM**](wmdm-enum-prop-valid-values-form.md) o, mejor aún, [**\_ \_ \_**](wmdm-prop-values-range.md) especificar un intervalo de formatos con la estructura WMDM PROP VALUES RANGE.

</dd> <dt>

**nChannels**
</dt> <dd>

Número de canales en los datos de audio de forma de onda. Los datos de los estados usan un canal y los datos estéreo usan dos canales.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Frecuencia de muestreo, en muestras por segundo (Hertz), en la que se debe reproducir o grabar cada canal. Los valores comunes de **nSamplesPerSec** son 8,0 kilohercios (kHz), 11,025 kHz, 22,05 kHz y 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Tasa media de transferencia de datos necesaria para la etiqueta de formato, en bytes por segundo. El software de reproducción y grabación puede calcular los tamaños de búfer mediante el **miembro nAvgBytesPerSec.**

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Alineación de bloques, en bytes. La alineación de bloques es la unidad atómica mínima de datos para el **tipo de formato wFormatTag.** El software de reproducción y grabación debe procesar un múltiplo de bytes **nBlockAlign** de datos a la vez. Los datos escritos y leídos desde un dispositivo siempre deben comenzar al principio de un bloque. Por ejemplo, no es posible empezar a reproducir correctamente los datos de PCM en medio de una muestra (es decir, en un límite que no está alineado en bloques).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits por ejemplo para el **tipo de formato wFormatTag.**

</dd> <dt>

**cbSize**
</dt> <dd>

Este miembro se omite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





