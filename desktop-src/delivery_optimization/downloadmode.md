---
title: Enumeración DownloadMode (Deliveryoptimization.h)
description: Define los distintos modos de descarga Optimización de distribución utiliza.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566773"
---
# <a name="downloadmode-enumeration"></a>Enumeración DownloadMode

Define los distintos modos de descarga Optimización de distribución utiliza.

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

Esta configuración deshabilita el almacenamiento en caché punto a punto, pero sigue Optimización de distribución descargar contenido de los servidores de Microsoft. Este modo usa metadatos adicionales proporcionados por Optimización de distribución cloud services para una experiencia de descarga confiable y eficaz sin pares.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Este modo de funcionamiento predeterminado de Optimización de distribución permite el uso compartido del mismo nivel en la misma red.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

Cuando se establece el modo de grupo, el grupo se selecciona automáticamente en función del sitio Active Directory Domain Services (AD DS) del dispositivo (Windows 10, versión 1607) o del dominio en el que se autentica el dispositivo (Windows 10, versión 1511). En el modo de grupo, el emparejamiento se produce entre subredes internas, entre dispositivos que pertenecen al mismo grupo, incluidos los dispositivos de las oficinas remotas. Puedes usar la opción GroupID para crear tu propio grupo personalizado independientemente de los dominios y sitios de AD DS. El modo de descarga en grupo es la opción recomendada para la mayoría de las organizaciones que tratan de conseguir la máxima optimización del ancho de banda con la Optimización de distribución.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Habilita orígenes del mismo nivel de Internet para Optimización de distribución.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

El modo simple deshabilita completamente el uso de los servicios en la nube de Optimización de distribución completo (para entornos sin conexión). Optimización de distribución cambia a este modo automáticamente cuando los servicios en la nube de Optimización de distribución no están disponibles, son inaccesibles o cuando el tamaño del archivo de contenido es inferior a 10 MB. En este modo, Optimización de distribución una experiencia de descarga confiable, sin almacenamiento en caché punto a punto.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

Omite Optimización de distribución y usa BITS en su lugar. Por ejemplo, selecciona este modo para que los clientes puedan usar BranchCache.

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|----------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>  |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>               |
