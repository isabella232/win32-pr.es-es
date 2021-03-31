---
description: La extensibilidad se consigue proporcionando el uso de nuevos identificadores de objeto (OID), nuevos tipos de codificación y nuevos archivos dll.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Información general sobre OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911585"
---
# <a name="oid-overview"></a>Información general sobre OID

La extensibilidad se consigue proporcionando el uso de nuevos [*identificadores de objeto*](../secgloss/o-gly.md) (OID), nuevos tipos de codificación y nuevos archivos dll.

Los OID de CryptoAPI pueden adoptar cualquiera de las siguientes formas:

-   Una cadena numérica como "1.2.3.500.88"
-   Una cadena alfanumérica como *myFunction*
-   Constante con un valor menor o igual que 0xFFFF. Estas constantes se suelen asociar a un nombre mediante el uso de una instrucción **\# define** en un archivo de encabezado.

Las funciones extensibles aceptan OID y los argumentos de tipo de codificación. Estas funciones buscan el registro del sistema para encontrar un archivo DLL asociado con el OID y los argumentos de tipo de codificación pasados a la función. Si se encuentra un archivo DLL para la combinación de tipo de codificación OID, el archivo DLL se carga y se llama a su función. En la siguiente ilustración se muestra este flujo para la función [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :

![flujo de OID](images/oidflow.png)

Esto permite que la funcionalidad de CryptoAPI se extienda a medida que sea necesario. El uso de esta metodología supone una carga para el desarrollador de la nueva funcionalidad para escribir todo el código necesario para esa funcionalidad. Para codificar una nueva estructura de datos, por ejemplo, la función de la DLL debe realizar todo el proceso de codificación.

 

 
