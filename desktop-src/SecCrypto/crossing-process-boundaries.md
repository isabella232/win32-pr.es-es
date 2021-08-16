---
description: El motor del protocolo Schannel realiza el protocolo de enlace y la autenticación en un proceso seguro y el cifrado masivo o el mensaje que pasa el proceso de aplicación.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Cruce de los límites del proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f8ba4c2d7a0a80ad97e62487421b5b4a0a6f8deda9d8edb550c2d8fcddab15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768889"
---
# <a name="crossing-process-boundaries"></a>Cruce de los límites del proceso

El [*motor del protocolo Schannel*](../secgloss/s-gly.md) realiza el protocolo [](../secgloss/p-gly.md) de enlace y la autenticación en un proceso seguro y el cifrado masivo o el mensaje que pasa el proceso de aplicación. Esto significa que las [*claves de cifrado masivo*](../secgloss/b-gly.md) y las claves [*MAC*](../secgloss/m-gly.md) deben copiarse de un proceso a otro. Para copiar las claves de un proceso a otro, use las funciones [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) y [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) como se muestra a continuación:

1.  El proceso seguro exporta cada clave a [*opaquekeyblob*](../secgloss/o-gly.md) mediante [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)y, a continuación, destruye la clave mediante [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Tenga en cuenta que si la clave se almacena en hardware, el CSP debe reconocerlo y no debe intentar destruir la clave.
2.  El proceso seguro pasa las opaquekeyblobs al proceso de aplicación de una manera más allá del ámbito de este documento.
3.  El proceso de aplicación importa cada opaquekeyblob de nuevo en el CSP mediante [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). En este momento, la clave debe estar exactamente en el mismo [*estado*](../secgloss/s-gly.md) que cuando se exportó.

 

 
