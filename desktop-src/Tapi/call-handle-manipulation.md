---
description: TAPI proporciona varias funciones para manipular los identificadores de llamada, determinar la relación entre las líneas, las llamadas y la dirección, etc.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Manipulación de identificadores de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687246"
---
# <a name="call-handle-manipulation"></a>Manipulación de identificadores de llamadas

TAPI proporciona varias funciones para manipular los identificadores de llamada, determinar la relación entre las líneas, las llamadas y la dirección, etc. La mayor parte de esta funcionalidad se implementa estrictamente en TAPI sin hacer referencia al proveedor de servicios, excepto para [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid). Esta función recupera el identificador de dirección de una llamada existente dentro de su línea. Los proveedores de servicios que modelan una línea como un grupo de identificadores de direcciones pueden elegir una dirección imprevisible para una nueva llamada entrante o saliente. Esta función proporciona información de TAPI suficiente para implementar la operación [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) cuando se invoca con la opción de \_ Dirección LINECALLSELECT.

 

 
