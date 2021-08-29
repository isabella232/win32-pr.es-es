---
title: Interfaces IAVIStream e IAVIFile
description: Interfaces IAVIStream e IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interfaz IAVIStream
- Interfaz IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f419de6864986bf72914dd5551ab6ad5b7093379b40180183171a7a498cea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140943"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Interfaces IAVIStream e IAVIFile

Las [**interfaces IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) [**e IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contienen los métodos utilizados por los controladores de archivos y secuencias. El tipo de datos **PAVISTREAM** es un puntero a un objeto de secuencia AVI (a través de la interfaz **IAVIStream)** y el tipo de datos **PAVIFILE** es un puntero a un objeto de archivo AVI (a través de la **interfaz IAVIFile).**

Para crear un puntero de objeto en C, asigne primero espacio para una estructura lo suficientemente grande como para contener el puntero a la tabla de función virtual y a los demás miembros de datos. Cree una tabla de funciones virtuales para los métodos para el tipo de secuencia y, a continuación, establezca el puntero a la tabla de funciones virtuales en la dirección de la tabla de funciones virtuales.

 

 




