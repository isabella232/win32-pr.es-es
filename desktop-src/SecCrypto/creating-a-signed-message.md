---
description: Describe las tareas que deben realizarse para crear un mensaje firmado.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Crear un mensaje firmado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277521"
---
# <a name="creating-a-signed-message"></a>Crear un mensaje firmado

En la ilustración siguiente se muestran las tareas que deben realizarse para crear un mensaje firmado. Los pasos se enumeran a continuación de la ilustración.

![firmar un mensaje](images/signdmsg.png)

**Para crear un mensaje firmado**

1.  Cree los datos (si es necesario) y obtenga un puntero a él.
2.  Abra un [*almacén de certificados*](../secgloss/c-gly.md) que contenga el certificado del firmante.
3.  Obtiene la [*clave privada*](../secgloss/p-gly.md) del certificado. Se debe establecer una propiedad en el certificado antes de utilizarla, para vincular un certificado a un [*CSP*](../secgloss/c-gly.md)determinado y, dentro de ese CSP, a una clave privada determinada. Debe establecerse una vez.
4.  Elija un algoritmo hash para la operación de resumen. Se recomienda seleccionar el algoritmo hash de una ubicación configurable que se puede actualizar posteriormente sin necesidad de realizar cambios en el código.
5.  Enviar los datos a través de la función de hash mediante el algoritmo hash, con lo que se crea un [*hash*](../secgloss/h-gly.md) (síntesis) de los datos.
6.  Mediante la [*clave privada*](../secgloss/p-gly.md) obtenida a través de la propiedad en el certificado, Cifre el Resumen y cree la firma.
7.  Incluya lo siguiente en el mensaje firmado:

    -   Los datos firmados
    -   Algoritmo hash
    -   La firma
    -   El identificador del firmante (emisor de certificados y número de serie)
    -   El certificado del firmante (opcional)

Para obtener un procedimiento detallado y un ejemplo, vea el [procedimiento para firmar datos](procedure-for-signing-data.md) y [el programa de ejemplo C: firmar un mensaje y comprobar la firma de un mensaje](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
