---
title: StorAHCI reemplaza a MSAHCI
description: StorAHCI reemplaza a MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932145"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI reemplaza a MSAHCI

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

StorAHCI, un minipuerto storport, admite controladores de interfaz avanzada de controlador de host (AHCI) de conexión de tecnología avanzada serie (SATA) en Windows y reemplaza a MSAHCI, un minipuerto ATAport.

## <a name="manifestation"></a>Manifestación

No debe haber ningún cambio en la funcionalidad o el rendimiento; este controlador admite todos los mismos dispositivos que admite MSAHCI.

Este cambio es transparente para el usuario.

## <a name="mitigation"></a>Mitigación

Actualice las utilidades y los scripts que se basan en enlaces ATAport. No se base en el nombre de la unidad. En su lugar, use la detección de disco estándar.

 

 




