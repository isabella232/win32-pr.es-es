---
description: Una aplicación TAPI debe llamar a una operación de inicialización, que solicita una serie de acciones de TAPI y los proveedores de servicios que configuran el entorno de comunicación de la aplicación.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inicialización principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688145"
---
# <a name="primary-initialization"></a>Inicialización principal

Una aplicación TAPI debe llamar a una operación de inicialización, que solicita una serie de acciones de TAPI y los proveedores de servicios que configuran el entorno de comunicación de la aplicación.

-   La inicialización es sincrónica y no devuelve ningún resultado hasta que se completa o se produce un error en la operación.
-   Si TAPISRV no se está ejecutando, TAPI lo inicia.
-   TAPI configura una conexión al proceso TAPISRV.
-   TAPISVR carga los proveedores de servicios especificados en el registro y les solicita que inicialicen los dispositivos que admiten.

**TAPI 2. x:** Las aplicaciones realizan la inicialización mediante una llamada a [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

**TAPI 3. x:** Las aplicaciones llaman a [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
