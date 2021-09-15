---
description: Use CertMgr para ver certificados, CRL y CL de un archivo o un almacén de certificados, copiar certificados en un almacén de certificados, eliminar certificados de un almacén de certificados y guardar certificados en archivos.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Uso de CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127477666"
---
# <a name="using-certmgr"></a>Uso de CertMgr

[CertMgr](certmgr.md) se puede usar para ver [*certificados,*](../secgloss/c-gly.md)listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) y listas de confianza de certificados [](../secgloss/c-gly.md) (CL) desde un archivo o un almacén de certificados, para copiar certificados en un almacén de [*certificados,*](../secgloss/c-gly.md)para eliminar certificados de un almacén de certificados y para guardar certificados en archivos.

Cuando [Se usa CertMgr](certmgr.md) sin opciones, aparece un asistente de CertMgr para guiar al usuario a través de la operación.

El archivo debe ser uno de los siguientes tipos:

-   Un archivo CTL, CRL o certificado codificado (podría estar codificado en base 64)
-   Un archivo PKCS \# 7
-   Un archivo SPC
-   Un documento firmado
-   Un storeFile serializado

En los ejemplos siguientes se [usan comandos de CertMgr](certmgr.md) para realizar tareas de certificado comunes.

-   Vea los certificados, las CRL y las CL *de MyFile.ext.*

    **certmgr** *MyFile.ext*

-   Vea los certificados, las CRL y las CL desde el almacén del sistema MY.

    **certmgr -s my**

-   Copie todos los certificados, CRL y CL de un archivo denominado *MyFile.ext* en un nuevo archivo, *denominado NewFile.ext.*

    **certmgr -add -all -c** *MyFile.ext* *NewFile.ext*

-   Copie todos los certificados, CRL y CL del almacén del sistema MY en un archivo *denominado NewMyFile.ext*.

    **certmgr -add -all -c -s my** *NewMyFile.ext*

-   Copie un certificado con el nombre común *MyCert* en el almacén del sistema MY en un archivo *denominado NewCert.cer*.

    **certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*

-   Elimine todos los certificados del almacén del sistema MY.

    **certmgr -del -all -c -s my**

-   Elimine todas las CL del almacén del sistema MY y guarde el almacén resultante en un archivo *denominado NewStore.str*.

    **certmgr -del -all -ctl -s my** *NewStore.str*

-   Guarde en un archivo denominado *NewCert.cer*, un certificado que sea un certificado codificado [*X.509,*](../secgloss/x-gly.md) que tenga el nombre común *MyCert* y que se encuentra en el almacén de certificados raíz.

    **certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
