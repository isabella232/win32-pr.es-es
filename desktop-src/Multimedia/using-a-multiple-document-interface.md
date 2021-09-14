---
title: Uso de una interfaz de varios documentos
description: Uso de una interfaz de varios documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Función MCIWndRegisterClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272271"
---
# <a name="using-a-multiple-document-interface"></a>Uso de una interfaz de varios documentos

Es posible que las aplicaciones que usan una interfaz de varios documentos (MDI) deban especificar estilos de ventana que no están disponibles a través de la [**función MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Para estas aplicaciones, puede registrar y crear una ventana MCIWnd mediante la función [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la [función CreateWindowEx.](/windows/win32/api/winuser/nf-winuser-createwindowexa) La **función MCIWndRegisterClass** registra la clase de ventana WINDOW CLASS de MCIWND y, a continuación, CreateWindowEx crea una instancia \_ de una ventana \_ MCIWnd. 

 

 