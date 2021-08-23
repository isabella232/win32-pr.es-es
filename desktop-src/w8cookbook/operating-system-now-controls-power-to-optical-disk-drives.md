---
title: El sistema operativo ahora controla la energía de las unidades de disco óptico.
description: El sistema operativo ahora controla la energía de las unidades de disco óptico.
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc43ad47f6a9468c2850627f267d433bfa346d059231d5daa91e860d5a793aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593805"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>El sistema operativo ahora controla la energía de las unidades de disco óptico.

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

En versiones anteriores de Windows, la energía de la unidad óptica no se administraba cuando la unidad óptica no estaba en uso. Ahora, si no hay ningún medio presente en la unidad de disco óptico (ODD), el sistema operativo apaga la alimentación a la unidad óptica. Esta característica se denomina IMPAR de potencia cero (ZPODD). La característica solo es aplicable a las unidades ópticas que usan un conector SATA deLine (serial advanced technology attachment).

## <a name="manifestation"></a>Manifestación

No hemos encontrado ningún impacto negativo de este nuevo comportamiento. sin embargo, debe ser consciente de ello, ya que puede dar lugar a un comportamiento inesperado del software de escritura multimedia.

## <a name="mitigation"></a>Mitigación

Para revertir al estado always-on, desactive esta funcionalidad en el Registro. La ruta de acceso absoluta al valor del Registro es:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Su tipo es DWORD (32 bits) y, si su valor es 0, ZPODD está deshabilitado; Si es cualquier otro valor, ZPODD está habilitado.

## <a name="tests"></a>Pruebas

Pruebe el software de escritura multimedia en busca de anomalías que se produzcan debido a esta nueva característica. Informe [a Microsoft de](mailto:OptIssue@microsoft.com) los problemas que encuentre con esta nueva característica.

 

 




