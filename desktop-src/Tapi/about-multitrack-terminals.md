---
description: Un terminal multipista se puede pensar como un terminal que es una colección de otros terminales. Cada terminal secundario (un &\# 0034;seguimiento&\# 0034;) puede ser un terminal multipista o un terminal de un solo seguimiento.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Acerca de los terminales multipista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa84537c3cf7764ba7e4520d32a325b89ad4dffd9921daa14bc5e0c968c7763f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872908"
---
# <a name="about-multitrack-terminals"></a>Acerca de los terminales multipista

Un terminal multipista se puede pensar como un terminal que es una colección de otros terminales. Cada terminal secundario (una "pista") puede ser un terminal multipista o un terminal de una sola pista.

Todos los terminales multipista exponen la interfaz [**ITMultiTrackTerminal,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) que incluye métodos genéricos para enumerar, crear y quitar terminales de seguimiento de un terminal multipista. Todos los terminales, de seguimiento único y multipista, exponen la [**interfaz ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)

Un cliente que tiene un puntero a una interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) puede detectar si el terminal es multipista o de un solo seguimiento consultando el terminal para la interfaz [**ITMultiTrackTerminal,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) que solo se expone en terminales multipista.

El terminal primario puede usar la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de sus terminales de seguimiento o puede requerir terminales de seguimiento para exponer interfaces privadas.

Para obtener más información, vea [Seguimiento de terminales.](track-terminals.md)

 

 
