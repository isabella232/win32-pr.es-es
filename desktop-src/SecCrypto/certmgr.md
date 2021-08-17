---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832610510eeb74b821ec690cab93fd9af74d69ca3479508b5c0707d45f491c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770012"
---
# <a name="certmgr"></a>CertMgr

Las herramientas de CertMgr reemplazan a DumpCert. Incluye nuevas funcionalidades para la administración de [*certificados,*](../secgloss/c-gly.md)listas de [*confianza*](../secgloss/c-gly.md) de certificados (CL) y listas [*de revocación de certificados*](../secgloss/c-gly.md) (CRL). La herramienta se instala en la carpeta Bin de la ruta de instalación de \\ Microsoft Windows Software Development Kit (SDK).

CertMgr está disponible como parte del SDK Windows, que puede descargar de <https://go.microsoft.com/fwlink/p/?linkid=84091> .

CertMgr realiza una de las cuatro funciones según la acción indicada en el comando .

**CertMgr** \[ **-add** \| **-del** \| **-put** \] \[  \] Opciones \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *DestinationName*\]

En la tabla siguiente se indican las acciones básicas de la herramienta CertMgr.



| Marca de acción | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno        | Muestra certificados, CRL o CTL. Sin ninguna marca de acción (solo para mostrar), *SourceName* es el nombre del almacén de certificados o el archivo que contiene los elementos que se mostrarán. El almacén puede ser un [*almacén serializado*](../secgloss/s-gly.md) (StoreFile) o un almacén del sistema. De forma predeterminada, CertMgr muestra todos los certificados, LASCL o CRL en el almacén de certificados o el archivo. *DestinationName* no se usa para mostrar.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -add        | Copia certificados, CCL y CRL en un almacén de certificados. Cuando se **usa -add**, *SourceName es* el almacén de certificados de origen que contiene los certificados, LASCL y CRL existentes. *DestinationName* es el almacén de certificados de destino al que se agregarán los certificados, LASCL y las CRL. El almacén de destino se guardará como un almacén serializado, [*a*](../secgloss/s-gly.md) menos que se utilice la opción **-7,** que guarda el almacén como [*un archivo PKCS*](../secgloss/p-gly.md) \# 7. Tenga en cuenta que **la opción -7** no se puede usar cuando el almacén de destino es un almacén del sistema.<br/>                                                                                                                          |
| -del        | Elimina certificados, CCL y CRL de un almacén de certificados. Cuando se **usa -del**, *SourceName* es el almacén de certificados de origen que contiene los certificados, LASCL y CRL existentes. *DestinationName* es el almacén de certificados de destino que contendrá copias del resto de certificados, CCL y CRL una vez eliminados los elementos especificados. Si no se especifica *DestinationName,* *SourceName* también actuará como almacén de destino (se modificará). El almacén de destino se guardará como un almacén serializado, [*a*](../secgloss/s-gly.md) menos que se utilice la opción **-7,** que guarda el almacén como un archivo PKCS \# 7. Tenga en cuenta que **la opción -7** no se puede usar cuando el almacén de destino es un almacén del sistema.<br/> |
| -put        | Guarda un [*certificado codificado X.509,*](../secgloss/x-gly.md) CTL o CRL en un archivo. Cuando se **usa -put**, *SourceName* es el almacén de certificados de origen que contiene los certificados existentes, las CL y las CRL. *DestinationName* es el nombre de un archivo en el que se guardará un certificado codificado [*X.509,*](../secgloss/x-gly.md) CTL y CRL. Si se **usa la opción -7,** el archivo se guardará como un archivo PKCS \# 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Opciones

Las siguientes opciones se aplican a todas las funciones de CertMgr, excepto donde se indica.



| Opción                     | Marca de acción                                 | Descripción                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | none (solo mostrar)                         | Modo detallado. Muestra información detallada sobre certificados, CCL y CRL. El valor predeterminado es mostrar información breve.                                                                                                                       |
| **-c**                     | todo                                         | Use solo certificados.                                                                                                                                                                                                                             |
| **-CTL**                   | todo                                         | Use solo las CL.                                                                                                                                                                                                                                     |
| **-CRL**                   | todo                                         | Use solo CRL.                                                                                                                                                                                                                                     |
| **-all**                   | **-add-del**<br/> **-put**<br/> | Agrega todas las entradas del tipo elegido.                                                                                                                                                                                                               |
| **-e** *encodingType*      | todo                                         | Tipo [*de codificación de certificado*](../secgloss/e-gly.md).                                                                                                                                             |
| **-y** *storeProviderType* | todo                                         | Tipo de proveedor de almacenamiento.                                                                                                                                                                                                                               |
| **-7**                     | **-add-del**<br/> **-put**<br/> | Guarda el almacén de destino como un archivo PKCS \# 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | todo                                         | Almacene la marca abierta. Este es el *parámetro dwFlags* pasado a [**CertOpenStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) El valor predeterminado es CERT \_ SYSTEM \_ STORE CURRENT \_ \_ USER. Significativo solo si **se establece -y.** Para obtener más información, **vea CertOpenStore.**         |
| **-n** *commonNameString*  | **-add-del**<br/> **-put**<br/> | Nombre común del certificado. Solo se puede usar con certificados.                                                                                                                                                                                |
| **-sha1** *sha1Hash*       | **-add-del**<br/> **-put**<br/> | Hash SHA1 del certificado, CTL o CRL que se va a copiar, eliminar o guardar.                                                                                                                                                                         |
| **-s**                     | todo                                         | Indica que el almacén es un almacén del sistema.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | todo                                         | Ubicación del Registro del almacén de certificados del sistema. Significativo solo cuando **se establece -s.** Debe establecerse en *currentUser* (clave del Registro HKEY CURRENT USER) o \_ \_ *localMachine* (clave del Registro HKEY \_ LOCAL \_ MACHINE). *currentUser* es el valor predeterminado. |
| **-?**                     | todo                                         | Muestra todas las opciones.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

CertMgr solo se admite en Internet Explorer 4.0 o posterior.

CertMgr puede copiar, eliminar o guardar uno o varios certificados, CCL o CRL. Si hay más de un elemento en una de estas categorías, el usuario tiene tres opciones:

-   Use la **opción -all** para copiar, eliminar o guardar todos los elementos de la categoría indicada.
-   Use las **opciones -n** **y -sha1** para identificar de forma única el elemento que se va a copiar, eliminar o guardar.
-   Si **no se indica -all**, o **-n** y **-sha1,** CertMgr solicita al usuario una lista de elementos para copiar, eliminar o guardar. El usuario responde especificando el índice del elemento que se va a copiar, eliminar o guardar.

Las acciones de CertMgr usan ligeras variaciones de la sintaxis y las opciones. Se deben usar la sintaxis y las opciones específicas de una acción.

CertMgr funciona con dos tipos de almacenes de certificados: StoreFile y el almacén del sistema. Un StoreFile puede ser uno de los siguientes tipos de archivos:

-   Un archivo CTL,CRL/certificate codificado (podría estar codificado en base 64)
-   Un archivo PKCS \# 7
-   Un documento firmado
-   StoreFile serializado

No es necesario especificar el tipo de StoreFile. CertMgr puede determinar el tipo StoreFile y realizar las acciones adecuadas.

Un almacén del sistema es un almacén de certificados que normalmente se encuentra en el Registro en **currentUser**. El usuario puede hacer referencia a un almacén del sistema proporcionando solo su nombre. No es necesario especificar el tipo de proveedor del almacén de certificados. En función del tipo de StoreFile o del almacén del sistema, CertMgr elige el tipo de proveedor de almacén correspondiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de CertMgr](using-certmgr.md)
</dt> </dl>

 

 
