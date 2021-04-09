---
title: Funciones de adquisición de claves
description: De forma predeterminada, el SSP suministra claves de cifrado a los programas de servidor que las solicitan. Cada SSP implementa su propio sistema de generación de claves. El formato de las claves que genera el SSP es específico del SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903775"
---
# <a name="key-acquisition-functions"></a>Funciones de adquisición de claves

De forma predeterminada, el SSP suministra claves de cifrado a los programas de servidor que las solicitan. Cada SSP implementa su propio sistema de generación de claves. El formato de las claves que genera el SSP es específico del SSP.

RPC le proporciona la capacidad de invalidar el método predeterminado de generación de claves de cifrado. La aplicación puede llamar a la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) y pasarle un puntero a una función de adquisición de clave. Puede escribir la función de adquisición de claves para que genere claves con cualquier método que elija. Sin embargo, la clave que pasa al programa de servidor debe coincidir con el formato que requiere el SSP.

> [!Note]  
> La mayoría de las aplicaciones no necesitan usar funciones de adquisición clave y simplemente pueden proporcionar **null** a todos los parámetros en los que se solicita una función de adquisición de claves.

 

 

 




