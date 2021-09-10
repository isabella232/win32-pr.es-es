---
title: Uso de una interfaz de varios documentos
description: Uso de una interfaz de varios documentos
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Función MCIWndRegisterClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372181"
---
# <a name="using-a-multiple-document-interface"></a>Uso de una interfaz de varios documentos

Es posible que las aplicaciones que usan una interfaz de múltiples documentos (MDI) deban especificar estilos de ventana que no están disponibles a través de la [**función MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Para estas aplicaciones, puede registrar y crear una ventana de MCIWnd mediante la función [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la [función CreateWindowEx.](/windows/win32/api/winuser/nf-winuser-createwindowexa) La **función MCIWndRegisterClass** registra la clase de ventana MCIWND WINDOW CLASS y, a continuación, CreateWindowEx crea una instancia de \_ una ventana \_ MCIWnd. 

 

 