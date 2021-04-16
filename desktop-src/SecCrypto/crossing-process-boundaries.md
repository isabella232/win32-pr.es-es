---
description: El motor del protocolo Schannel realiza el enlace y la autenticación en un proceso seguro y el cifrado o mensaje de forma masiva en el proceso de la aplicación.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Cruzar los límites del proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686690"
---
# <a name="crossing-process-boundaries"></a>Cruzar los límites del proceso

El motor del protocolo [*Schannel*](../secgloss/s-gly.md) realiza el enlace y la autenticación en un [*proceso*](../secgloss/p-gly.md) seguro y el cifrado o mensaje de forma masiva en el proceso de la aplicación. Esto significa que las [*claves de cifrado masivo*](../secgloss/b-gly.md) y las claves [*Mac*](../secgloss/m-gly.md) se deben copiar de un proceso a otro. Para copiar las claves de un proceso a otro, utilice las funciones [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) y [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) como se indica a continuación:

1.  El proceso seguro exporta cada clave a un [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)y, a continuación, destruye la clave mediante [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Tenga en cuenta que si la clave se almacena en hardware, el CSP debe reconocerlo y no debe intentar destruir la clave.
2.  El proceso seguro pasa el OPAQUEKEYBLOBs al proceso de la aplicación de una forma más allá del ámbito de este documento.
3.  El proceso de aplicación importa cada OPAQUEKEYBLOB de vuelta al CSP mediante [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). En este punto, la clave debe estar exactamente en el mismo [*Estado*](../secgloss/s-gly.md) en que se exportó.

 

 
