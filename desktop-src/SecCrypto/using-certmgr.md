---
description: Use CertMgr para ver certificados, CRL y CTL desde un archivo o un almacén de certificados, para copiar certificados en un almacén de certificados, para eliminar certificados de un almacén de certificados y para guardar certificados en archivos.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Usar CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666723"
---
# <a name="using-certmgr"></a>Usar CertMgr

[Certmgr](certmgr.md) se puede usar para ver [*certificados*](../secgloss/c-gly.md), [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) y [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL) de un archivo o un almacén de certificados, para copiar certificados en un [*almacén*](../secgloss/c-gly.md)de certificados, eliminar certificados de un almacén de certificados y guardar certificados en archivos.

Cuando se usa [Certmgr](certmgr.md) sin opciones, aparece un asistente de Certmgr para guiar al usuario a través de la operación.

El archivo debe ser uno de los siguientes tipos:

-   Una CTL codificada, una CRL o un archivo de certificado (se puede codificar en base 64)
-   Un \# archivo PKCS 7
-   Un archivo SPC
-   Un documento firmado
-   Un storeFile serializado

En los ejemplos siguientes se usan los comandos de [Certmgr](certmgr.md) para realizar tareas comunes de certificado.

-   Vea los certificados, las CRL y las CTL de *archivos. ext*.

    **Certmgr** *. ext*

-   Vea los certificados, las CRL y las CTL del almacén del sistema.

    **Certmgr-s mi**

-   Copie todos los certificados, CRL y listas CTL de un archivo llamado archivo *. ext* en un archivo nuevo, denominado *NewFile. ext*.

    **Certmgr-Add-All-c** *archivo. ext* *NewFile. ext*

-   Copie todos los certificados, CRL y listas CTL del almacén del sistema MY en un archivo denominado *NewMyFile. ext*.

    **Certmgr-Add-All-c-s mis** *NewMyFile. ext*

-   Copie un certificado con el nombre común *mycert* en mi almacén del sistema en un archivo denominado *NewCert. cer*.

    **Certmgr-Add-c-n** *mycert* **-s My** *NewCert. cer*

-   Elimine todos los certificados de mi almacén del sistema.

    **Certmgr-del-todos-c-s mi**

-   Elimine todas las CTL del almacén del sistema MY y guarde el almacén resultante en un archivo denominado *NewStore. Str*.

    **Certmgr-del-All-CTL-s My** *NewStore. Str*

-   Guardar, en un archivo denominado *NewCert. cer*, un certificado que es un certificado codificado [*X. 509*](../secgloss/x-gly.md) , que tiene el nombre común *mycert* y que se encuentra en el almacén de certificados raíz.

    **Certmgr-Put-c-n** *mycert* **-s raíz** *NewCert. cer*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
