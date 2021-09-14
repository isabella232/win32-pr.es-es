---
description: Una aplicación TAPI debe llamar a una operación de inicialización, que solicita una serie de acciones de TAPI y los proveedores de servicios que configuraron el entorno de comunicación para la aplicación.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inicialización principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173082"
---
# <a name="primary-initialization"></a>Inicialización principal

Una aplicación TAPI debe llamar a una operación de inicialización, que solicita una serie de acciones de TAPI y los proveedores de servicios que configuraron el entorno de comunicación para la aplicación.

-   La inicialización es sincrónica y no se devuelve hasta que la operación se completa o se ha dado error.
-   Si TAPISRV aún no se está ejecutando, TAPI lo inicia.
-   TAPI configura una conexión al proceso TAPISRV.
-   TAPISVR carga los proveedores de servicios especificados en el registro y les pide que inicialicen los dispositivos que admiten.

**TAPI 2.x:** Las aplicaciones realizan la inicialización mediante [**una llamada a lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

**TAPI 3.x:** Las aplicaciones llaman [**a ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
