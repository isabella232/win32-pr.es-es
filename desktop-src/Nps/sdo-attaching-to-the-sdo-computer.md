---
title: Asociación al equipo SDO
description: Con el puntero de interfaz devuelto por CoCreateInstance, llame al método ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5863302da3f213c1360c254782a31c0dfc4fcb9a946f5827155862bca01405cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362193"
---
# <a name="attaching-to-the-sdo-computer"></a>Asociación al equipo SDO

Con el puntero de interfaz devuelto por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), llame al [**método ISdoMachine::Attach.**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) Pase **NULL** como parámetro al **método Attach.** El valor **NULL** especifica que **Attach asocie** el objeto de máquina con el equipo local. No se admite la asociación a un equipo remoto.

Para determinar si el equipo local ya está asociado, llame al [**método ISdoMachine::GetAttachedComputer.**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer)

Vea [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) (Adjuntar a un equipo de SDO-Enabled) para obtener código de ejemplo que muestra cómo conectarse al equipo local.

 

 