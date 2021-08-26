---
title: Funciones de adquisición de claves
description: De forma predeterminada, el SSP proporciona claves de cifrado a los programas de servidor que las solicitan. Cada SSP implementa su propio sistema de generación de claves. El formato de las claves que genera el SSP es específico del SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292926f53e5af0e75957f9b363d3917b1c5f68ef3a4e0a0acf7111c6b37b6518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020238"
---
# <a name="key-acquisition-functions"></a>Funciones de adquisición de claves

De forma predeterminada, el SSP proporciona claves de cifrado a los programas de servidor que las solicitan. Cada SSP implementa su propio sistema de generación de claves. El formato de las claves que genera el SSP es específico del SSP.

RPC proporciona la capacidad de invalidar el método predeterminado para generar claves de cifrado. La aplicación puede llamar a [**la función RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) y pasarle un puntero a una función de adquisición de claves. Puede escribir la función de adquisición de claves para que genere claves mediante cualquier método que elija. Sin embargo, la clave que pasa al programa de servidor debe coincidir con el formato que requiere el SSP.

> [!Note]  
> La mayoría de las aplicaciones no necesitan usar funciones de adquisición de claves y simplemente pueden proporcionar **NULL** a todos los parámetros en los que se solicita una función de adquisición de claves.

 

 

 




