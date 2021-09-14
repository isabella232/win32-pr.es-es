---
description: La extensibilidad se logra al proporcionar el uso de nuevos identificadores de objeto ( DLL), nuevos tipos de codificación y nuevos archivos DLL.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Introducción a OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173157"
---
# <a name="oid-overview"></a>Introducción a OID

La extensibilidad se logra al proporcionar el uso de nuevos identificadores de objeto [*(*](../secgloss/o-gly.md) DLL), nuevos tipos de codificación y nuevos archivos DLL.

Los ID de CryptoAPI pueden tomar cualquiera de las formas siguientes:

-   Cadena numérica como "1.2.3.500.88"
-   Una cadena alfanumérica como *MyFunction*
-   Constante con un valor menor o igual que 0xFFFF. Estas constantes se suelen asociar a un nombre mediante el uso de una **\# instrucción define** en un archivo de encabezado.

Las funciones extensibles aceptan argumentos de tipo de codificación y OID. Estas funciones buscan en el Registro del sistema un archivo DLL asociado al OID y a los argumentos de tipo de codificación pasados a la función. Si se encuentra un archivo DLL para el OID, se encuentra la combinación de tipos de codificación, se carga el archivo DLL y se llama a su función. En la ilustración siguiente se muestra este flujo para la [**función CryptEncodeObject:**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)

![Flujo de oid](images/oidflow.png)

Esto permite ampliar la funcionalidad de CryptoAPI a medida que surge la necesidad. El uso de esta metodología supone una carga para el desarrollador de la nueva funcionalidad para escribir todo el código necesario para esa funcionalidad. Para codificar alguna nueva estructura de datos, por ejemplo, la función del archivo DLL debe realizar todo el proceso de codificación.

 

 
