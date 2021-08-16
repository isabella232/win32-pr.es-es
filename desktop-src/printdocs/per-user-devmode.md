---
description: Un usuario puede especificar la configuración predeterminada del documento para una impresora. Esto se denomina DEVMODE por usuario porque solo afecta a los valores predeterminados de un usuario determinado y la información de cada impresora se define en una estructura DEVMODE independiente.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731934"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

Un usuario puede especificar la configuración predeterminada del documento para una impresora. Esto se denomina *DEVMODE* por usuario porque solo afecta a los valores predeterminados de un usuario determinado y la información de cada impresora se define en una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) independiente.

Para establecer el DEVMODE por usuario, llame a [**SetPrinter**](setprinter.md) con la estructura [**PRINTER INFO \_ \_ 2**](printer-info-2.md) o [**PRINTER INFO \_ \_ 9.**](printer-info-9.md) Para restablecer el DEVMODE por usuario al valor predeterminado global [**DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea)llame a **SetPrinter** con la [**estructura PRINTER INFO \_ \_ 8.**](printer-info-8.md)

 

 



