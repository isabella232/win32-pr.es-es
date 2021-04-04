---
title: Usar una interfaz de varios documentos
description: Usar una interfaz de varios documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904572"
---
# <a name="using-a-multiple-document-interface"></a>Usar una interfaz de varios documentos

Es posible que las aplicaciones que usan una interfaz de múltiples documentos (MDI) necesiten especificar estilos de ventana que no están disponibles a través de la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Para estas aplicaciones, puede registrar y crear una ventana MCIWnd mediante la función [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la función [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) . La función **MCIWndRegisterClass** registra la \_ \_ clase de ventana de clase de ventana MCIWND y, a continuación, **CreateWindowEx** crea una instancia de una ventana de MCIWND.

 

 