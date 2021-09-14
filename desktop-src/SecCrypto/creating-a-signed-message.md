---
description: Muestra las tareas que se deben realizar para crear un mensaje firmado.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Crear un mensaje firmado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259564"
---
# <a name="creating-a-signed-message"></a>Crear un mensaje firmado

En la ilustración siguiente se muestran las tareas que se deben realizar para crear un mensaje firmado. Los pasos se enumeran a continuación de la ilustración.

![firmar un mensaje](images/signdmsg.png)

**Para crear un mensaje firmado**

1.  Cree los datos (si es necesario) y obtenga un puntero a él.
2.  Abra un [*almacén de certificados*](../secgloss/c-gly.md) que contenga el certificado del firmante.
3.  Obtenga la [*clave privada*](../secgloss/p-gly.md) del certificado. Se debe establecer una propiedad en el certificado antes de usarlo, para vincular un certificado a un [*CSP*](../secgloss/c-gly.md)determinado y, dentro de ese CSP, a una clave privada determinada. Debe establecerse una vez.
4.  Elija un algoritmo hash para la operación de resumen. Se recomienda seleccionar el algoritmo hash desde una ubicación configurable que se pueda actualizar posteriormente sin necesidad de realizar cambios en el código.
5.  Envíe los datos a través de la función hash mediante el algoritmo hash, lo que crea un [*hash*](../secgloss/h-gly.md) (resumen) de los datos.
6.  Con la [*clave privada obtenida*](../secgloss/p-gly.md) a través de la propiedad en el certificado, cifre el resumen y cree la firma.
7.  Incluya lo siguiente en el mensaje firmado:

    -   Los datos firmados
    -   Algoritmo hash
    -   La firma
    -   Identificador del firmante (emisor del certificado y número de serie)
    -   Certificado del firmante (opcional)

Para obtener un procedimiento y un ejemplo detallados, vea [Procedimiento](procedure-for-signing-data.md) para firmar datos y Programa C de [ejemplo: Firmar](example-c-program-signing-a-message-and-verifying-a-message-signature.md)un mensaje y Comprobar una firma de mensaje .

 

 
