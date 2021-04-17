---
title: StorAHCI reemplaza a MSAHCI
description: StorAHCI reemplaza a MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105705055"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI reemplaza a MSAHCI

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

StorAHCI, un minipuerto Storport, es compatible con los controladores de la interfaz de controlador de hosts (AHCI) avanzada de Serial Advanced Technology Attachment (SATA) en Windows y reemplaza MSAHCI, un minipuerto ATAport.

## <a name="manifestation"></a>Manifestación

No debe haber ningún cambio en la funcionalidad o el rendimiento; Este controlador es compatible con todos los dispositivos que admite MSAHCI.

Este cambio es transparente para el usuario.

## <a name="mitigation"></a>Mitigación

Actualice las utilidades y los scripts que se basan en los enlaces de ATAport. No se base en el nombre de la unidad. En su lugar, use la detección de disco estándar.

 

 




