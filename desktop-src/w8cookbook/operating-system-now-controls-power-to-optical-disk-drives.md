---
title: El sistema operativo controla ahora las unidades de disco ópticos de energía
description: El sistema operativo controla ahora las unidades de disco ópticos de energía
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794200"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>El sistema operativo controla ahora las unidades de disco ópticos de energía

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

En versiones anteriores de Windows, la capacidad de la unidad óptica no se administraba cuando la unidad óptica no estaba en uso. Ahora, si no hay ningún medio en la unidad de disco óptico (IMPAr), el sistema operativo apaga la alimentación de la unidad óptica. Esta característica se denomina sin fuerza de energía (ZPODD). La característica solo es aplicable a las unidades ópticas que usan un conector SATA Slimline (Serial Advanced Technology Attachment).

## <a name="manifestation"></a>Manifestación

No hemos encontrado ningún impacto negativo en este nuevo comportamiento; sin embargo, debe ser consciente de ello, ya que puede dar lugar a un comportamiento inesperado del software de escritura de medios.

## <a name="mitigation"></a>Mitigación

Para revertir al estado AlwaysOn, desactive esta funcionalidad en el registro. La ruta de acceso absoluta al valor del registro es:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Su tipo es DWORD (32 bits) y si su valor es 0, ZPODD está deshabilitado; Si se trata de cualquier otro valor, ZPODD está habilitado.

## <a name="tests"></a>Pruebas

Pruebe el software de escritura multimedia para detectar las anomalías que se produzcan debido a esta nueva característica. [Informe a Microsoft](mailto:OptIssue@microsoft.com) de los problemas que encuentre con esta nueva característica.

 

 




