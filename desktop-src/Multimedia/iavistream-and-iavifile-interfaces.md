---
title: Interfaces IAVIStream y IAVIFile
description: Interfaces IAVIStream y IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interfaz IAVIStream
- Interfaz IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903581"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Interfaces IAVIStream y IAVIFile

Las interfaces [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) y [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contienen los métodos que usan los controladores de archivos y secuencias. El tipo de datos **PAVISTREAM** es un puntero a un objeto de flujo AVI (a través de la interfaz **IAVIStream** ) y el tipo de datos **PAVIFILE** es un puntero a un objeto de archivo AVI (a través de la interfaz **IAVIFile** ).

Para crear un puntero de objeto en C, asigne primero el espacio para una estructura que sea lo suficientemente grande como para contener el puntero a la tabla de funciones virtuales y los demás miembros de datos. Cree una tabla de función virtual para los métodos del tipo de secuencia y, a continuación, establezca el puntero en la tabla de función virtual en la dirección de la tabla de función virtual.

 

 




