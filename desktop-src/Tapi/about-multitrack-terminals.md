---
description: Un terminal multipista se puede considerar como un terminal que es una colección de otros terminales. Cada terminal secundario (un &\# 0034; track&\# 0034;) puede ser un terminal Multipista o un terminal de una sola pista.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Acerca de los terminales multipista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677816"
---
# <a name="about-multitrack-terminals"></a>Acerca de los terminales multipista

Un terminal multipista se puede considerar como un terminal que es una colección de otros terminales. Cada terminal secundario (una "pista") puede ser un terminal Multipista o un terminal de una sola pista.

Todos los terminales multipista exponen la interfaz [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que incluye métodos genéricos para enumerar, crear y quitar terminales de seguimiento de un terminal multipista. Todos los terminales, una sola pista y una Multipista, exponen la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

Un cliente que tiene un puntero a una interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) puede detectar si el terminal es Multipista o de una sola pista; para ello, consulta el terminal de la interfaz [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que solo se expone en terminales multipista.

El terminal principal puede usar la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de sus terminales de seguimiento o puede requerir que los terminales de seguimiento expongan interfaces privadas.

Para obtener más información, consulte [seguimiento de terminales](track-terminals.md).

 

 
