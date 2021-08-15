---
title: Consideraciones de seguridad del Sistema de colores de Windows
description: Consideraciones de seguridad del Sistema de colores de Windows
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Sistema de colores (WCS), seguridad
- WCS (Windows de color), seguridad
- administración de colores de imagen, seguridad
- administración de colores, seguridad
- seguridad para Windows Color System (WCS)
- Módulo de administración de colores (CMM)
- CMM (módulo de administración de colores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e710a0224c10d4f7cd7aa1565e88d00da539370974719129a37d735f11a29fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444672"
---
# <a name="security-considerations-windows-color-system"></a>Consideraciones de seguridad: Windows Color System

En este documento se proporciona información sobre las consideraciones de seguridad relacionadas con la administración del color de la imagen. Este documento no proporciona todo lo que necesita saber sobre los problemas de seguridad; en su lugar, úselo como punto de partida y referencia para esta área tecnológica.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>Los CMM que no son de Microsoft se pueden ejecutar en el contexto del sistema

Los módulos de administración de colores (CMM) que no son de Microsoft deben tratarse como controladores de impresora que no son de Microsoft porque tienen la posibilidad de ejecutarse en un contexto del sistema para las operaciones de impresión.
