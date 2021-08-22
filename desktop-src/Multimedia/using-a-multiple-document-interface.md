---
title: Uso de una interfaz de varios documentos
description: Uso de una interfaz de varios documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Función MCIWndRegisterClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941060"
---
# <a name="using-a-multiple-document-interface"></a>Uso de una interfaz de varios documentos

Es posible que las aplicaciones que usan una interfaz de múltiples documentos (MDI) deban especificar estilos de ventana que no están disponibles a través de la [**función MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Para estas aplicaciones, puede registrar y crear una ventana de MCIWnd mediante la función [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la [función CreateWindowEx.](/windows/win32/api/winuser/nf-winuser-createwindowexa) La **función MCIWndRegisterClass** registra la clase de ventana MCIWND WINDOW CLASS y, a continuación, CreateWindowEx crea una instancia de \_ una ventana \_ MCIWnd. 

 

 