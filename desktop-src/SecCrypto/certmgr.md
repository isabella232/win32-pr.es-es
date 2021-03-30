---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e248aef1f726b16d8f17098cfc9642393b963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156284"
---
# <a name="certmgr"></a>CertMgr

Las herramientas de CertMgr reemplazan a DumpCert. Incluye nuevas capacidades para la administración de [*certificados*](../secgloss/c-gly.md), [*listas*](../secgloss/c-gly.md) de certificados de confianza (CTL) y [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL). La herramienta se instala en la \\ carpeta bin de la ruta de instalación del kit de desarrollo de software (SDK) de Microsoft Windows.

CertMgr está disponible como parte del Windows SDK, que puede descargar de <https://go.microsoft.com/fwlink/p/?linkid=84091> .

CertMgr realiza una de las cuatro funciones según la acción indicada en el comando.

**Certmgr** \[ **-Agregar** \| **-del** \| **-Put** \] \[  Opciones \] de \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *DestinationName*\]

En la tabla siguiente se indican las acciones básicas de la herramienta CertMgr.



| Marca de acción | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno        | Muestra certificados, listas CRL o CTL. sin marca de acción (para mostrar solo), *SourceName* es el nombre del almacén de certificados o el archivo que contiene los elementos que se van a mostrar. El almacén puede ser un almacén [*serializado*](../secgloss/s-gly.md) (StoreFile) o un almacén del sistema. De forma predeterminada, CertMgr muestra todos los certificados, las CTL o las CRL del almacén de certificados o el archivo. *DestinationName* no se utiliza para la presentación.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -Agregar        | Copia certificados, listas CTL y listas CRL en un almacén de certificados. Cuando se usa **-Add**, *SourceName* es el almacén de certificados de origen que contiene los certificados, las CTL y las listas CRL existentes. *DestinationName* es el almacén de certificados de destino al que se agregarán los certificados, las CTL y las CRL. El almacén de destino se guardará como un almacén [*serializado*](../secgloss/s-gly.md) , a menos que se use la opción **-7** , que guarda el almacén como un archivo [*PKCS*](../secgloss/p-gly.md) \# 7. Tenga en cuenta que la opción **-7** no se puede usar cuando el almacén de destino es un almacén del sistema.<br/>                                                                                                                          |
| -del        | Elimina certificados, listas CTL y listas CRL de un almacén de certificados. Cuando se usa **-del**, *SourceName* es el almacén de certificados de origen que contiene los certificados, las CTL y las listas CRL existentes. *DestinationName* es el almacén de certificados de destino que contendrá copias de los certificados, CTL y listas CRL restantes una vez eliminados los elementos especificados. Si no se especifica *DestinationName* , *SourceName* también servirá como almacén de destino (se modificará). El almacén de destino se guardará como un almacén [*serializado*](../secgloss/s-gly.md) , a menos que se use la opción **-7** , que guarda el almacén como un \# archivo PKCS 7. Tenga en cuenta que la opción **-7** no se puede usar cuando el almacén de destino es un almacén del sistema.<br/> |
| -Put        | Guarda un certificado codificado [*X. 509*](../secgloss/x-gly.md) , una CTL o una CRL en un archivo. Cuando se usa **-Put**, *SourceName* es el almacén de certificados de origen que contiene los certificados, las CTL y las listas CRL existentes. *DestinationName* es el nombre de un archivo en el que se guardará un certificado codificado [*X. 509*](../secgloss/x-gly.md) , CTL y CRL. Si se usa la opción **-7** , el archivo se guardará como un \# archivo PKCS 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Opciones

Las siguientes opciones se aplican a todas las funciones de CertMgr excepto donde se indique.



| Opción                     | Marca de acción                                 | Descripción                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | ninguno (solo mostrar)                         | Modo detallado. Muestra información detallada acerca de los certificados, las CTL y las CRL. El valor predeterminado es Mostrar información breve.                                                                                                                       |
| **-c**                     | todo                                         | Usar solo certificados.                                                                                                                                                                                                                             |
| **-CTL**                   | todo                                         | Usar solo CTL.                                                                                                                                                                                                                                     |
| **-CRL**                   | todo                                         | Usar solo CRL.                                                                                                                                                                                                                                     |
| **-todo**                   | **-Add-del**<br/> **-Put**<br/> | Agrega todas las entradas del tipo elegido.                                                                                                                                                                                                               |
| **-e** *encodingType*      | todo                                         | [*Tipo de codificación*](../secgloss/e-gly.md)de certificado.                                                                                                                                             |
| **-y** *storeProviderType* | todo                                         | Tipo de proveedor de almacenamiento.                                                                                                                                                                                                                               |
| **-7**                     | **-Add-del**<br/> **-Put**<br/> | Guarda el almacén de destino como un \# archivo PKCS 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | todo                                         | Marca de apertura de la tienda. Este es el parámetro *dwFlags* que se pasa a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore). El valor predeterminado es el \_ usuario actual del almacén del sistema de certificados \_ \_ \_ . Solo tiene sentido si se establece **-y** . Para obtener más información, consulte **CertOpenStore**.         |
| **-n** *commonNameString*  | **-Add-del**<br/> **-Put**<br/> | Nombre común del certificado. Solo se puede usar con certificados.                                                                                                                                                                                |
| **-SHA1** *sha1Hash*       | **-Add-del**<br/> **-Put**<br/> | Hash SHA1 del certificado, CTL o CRL que se va a copiar, eliminar o guardar.                                                                                                                                                                         |
| **-s**                     | todo                                         | Indica que el almacén es un almacén del sistema.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | todo                                         | Ubicación del registro del almacén de certificados del sistema. Solo tiene sentido cuando se establece **-s** . Debe establecerse en *currentUser* (clave del registro HKEY \_ Current \_ User) o *LOCALMACHINE* (clave del registro HKEY \_ local \_ Machine). *currentUser* es el valor predeterminado. |
| **-?**                     | todo                                         | Muestra todas las opciones.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

CertMgr solo se admite en Internet Explorer 4,0 o posterior.

CertMgr puede copiar, eliminar o guardar uno o más certificados, CTL o CRL. Si hay más de un elemento en una de estas categorías, el usuario tiene tres opciones:

-   Use la opción **-All** para copiar, eliminar o guardar todos los elementos de la categoría indicada.
-   Use las opciones **-n** y **-SHA1** para identificar de forma única el elemento que se va a copiar, eliminar o guardar.
-   Si **-All**, o **-n** y **-SHA1** no se indican, Certmgr solicita al usuario una lista de elementos para copiar, eliminar o guardar. El usuario responde especificando el índice del elemento que se va a copiar, eliminar o guardar.

Las acciones de CertMgr usan ligeras variaciones de la sintaxis y las opciones. Se deben usar la sintaxis y las opciones específicas de una acción.

CertMgr funciona con dos tipos de almacenes de certificados: StoreFile y almacén del sistema. StoreFile puede ser uno de los siguientes tipos de archivos:

-   Un archivo CTL/CRL/certificado codificado (puede tener la codificación base 64)
-   Un \# archivo PKCS 7
-   Un documento firmado
-   Un StoreFile serializado

No es necesario especificar el tipo de StoreFile. CertMgr puede determinar el tipo de StoreFile y tomar las medidas adecuadas.

Un almacén del sistema es un almacén de certificados que normalmente se encuentra en el registro en **currentUser**. El usuario puede hacer referencia a un almacén del sistema proporcionando simplemente su nombre. No es necesario especificar el tipo de proveedor de almacén de certificados. En función del tipo de StoreFile o del almacén del sistema, CertMgr elige el tipo de proveedor de almacén correspondiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar CertMgr](using-certmgr.md)
</dt> </dl>

 

 
