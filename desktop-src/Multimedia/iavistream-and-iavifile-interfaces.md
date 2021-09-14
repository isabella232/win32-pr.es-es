---
title: Interfaces IAVIStream e IAVIFile
description: Interfaces IAVIStream e IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interfaz IAVIStream
- IAVIFile (interfaz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062911"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Interfaces IAVIStream e IAVIFile

Las [**interfaces IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) [**e IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contienen los métodos usados por los controladores de archivos y secuencias. El tipo de datos **PAVISTREAM** es un puntero a un objeto de flujo AVI (a través de la interfaz **IAVIStream)** y el tipo de datos **PAVIFILE** es un puntero a un objeto de archivo AVI (a través de la interfaz **IAVIFile).**

Para crear un puntero de objeto en C, asigne primero espacio para una estructura lo suficientemente grande como para contener el puntero a la tabla de función virtual y a los demás miembros de datos. Cree una tabla de funciones virtuales para los métodos del tipo de secuencia y, a continuación, establezca el puntero a la tabla de funciones virtuales en la dirección de la tabla de funciones virtuales.

 

 




