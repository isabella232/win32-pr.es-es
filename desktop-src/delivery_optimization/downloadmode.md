---
title: Enumeración DownloadMode (Deliveryoptimization. h)
description: Define los diferentes modos de descarga que utiliza la optimización de entrega.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Omite Optimización de distribución y usa BITS en su lugar. Por ejemplo, selecciona este modo para que los clientes puedan usar BranchCache. enumeración
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079290"
---
# <a name="downloadmode-enumeration"></a>Enumeración DownloadMode

Define los diferentes modos de descarga que utiliza la optimización de entrega.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

Esta configuración deshabilita el almacenamiento en caché del mismo nivel, pero permite que la optimización de entrega Descargue contenido de servidores de Microsoft. Este modo utiliza metadatos adicionales proporcionados por los servicios en la nube de optimización de entrega para una experiencia de descarga eficaz y confiable.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Este modo de funcionamiento predeterminado de Optimización de distribución permite el uso compartido del mismo nivel en la misma red.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

Cuando se establece el modo de grupo, el grupo se selecciona automáticamente según el sitio de Active Directory Domain Services de dispositivos (AD DS) (Windows 10, versión 1607) o el dominio al que se autentica el dispositivo (Windows 10, versión 1511). En el modo de grupo, el emparejamiento se produce entre subredes internas, entre dispositivos que pertenecen al mismo grupo, incluidos los dispositivos de las oficinas remotas. Puedes usar la opción GroupID para crear tu propio grupo personalizado independientemente de los dominios y sitios de AD DS. El modo de descarga en grupo es la opción recomendada para la mayoría de las organizaciones que tratan de conseguir la máxima optimización del ancho de banda con la Optimización de distribución.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Habilita orígenes del mismo nivel de Internet para Optimización de distribución.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

El modo simple deshabilita completamente el uso de los servicios en la nube de Optimización de distribución completo (para entornos sin conexión). La optimización de entrega cambia a este modo automáticamente cuando los servicios en la nube de optimización de entrega no están disponibles, no se puede tener acceso a ellos o cuando el tamaño del archivo de contenido es inferior a 10 MB. En este modo, la optimización de entrega proporciona una experiencia de descarga confiable, sin almacenamiento en caché punto a punto.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

Omite Optimización de distribución y usa BITS en su lugar. Por ejemplo, selecciona este modo para que los clientes puedan usar BranchCache.

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|----------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>  |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
