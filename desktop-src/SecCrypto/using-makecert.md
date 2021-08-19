---
description: Use los comandos MakeCert para crear certificados de prueba mediante las opciones disponibles Internet Explorer versión 4.0 o posterior.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Uso de MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321eccfc26e3fc5bf13a541e1aab6a41b3f5d0930beed03f6033211bf63ac689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971556"
---
# <a name="using-makecert"></a>Uso de MakeCert

En los ejemplos siguientes se [usan comandos MakeCert](makecert.md) para crear certificados de prueba mediante las opciones disponibles Internet Explorer versión 4.0 o posterior.

-   Crear un certificado emitido por la raíz de prueba predeterminada. Guarde el certificado en un archivo.

    **MakeCert** *MyNew.cer*

-   Crear un certificado emitido por la raíz de prueba predeterminada. Guárdelo en un almacén de certificados.

    **MakeCert -ss** *MyNewStore*

-   Crear un certificado emitido por la raíz de prueba predeterminada. Cree un contenedor de claves y guarde el certificado en un almacén y en un archivo.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*

-   Crear un certificado emitido por la raíz de prueba predeterminada. Cree un archivo de clave privada y guarde el certificado en un almacén y en un archivo.

    **MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*

-   Crear un certificado emitido por la raíz de prueba predeterminada. Cree un contenedor de claves, guarde el certificado en un almacén y un archivo y haga que la clave privada sea exportable.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**

-   Crear un certificado mediante la raíz de prueba predeterminada. Guarde el certificado en un almacén. A continuación, cree otro certificado emitido por el certificado recién creado. Guarde el segundo certificado en otro almacén.

    **MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*

-   Crear un certificado mediante la raíz de prueba predeterminada. Guarde el certificado en el almacén MY. A continuación, cree otro certificado mediante el certificado recién creado. Si hay más de un certificado en el almacén MY, el certificado debe identificarse con su nombre común.

    **MakeCert -sk** *MyNewKey* **-n "CN=XX SKUY" -ss my MakeCert -is my -in "XX SKUY" -ss** *AnotherStore*

-   Crear un certificado mediante la raíz de prueba predeterminada. Guarde el certificado en el almacén MY y en un archivo. A continuación, cree otro certificado mediante el certificado *MyNew recién* creado. Si hay más de un certificado en el almacén MY, identifique de forma única el primer certificado mediante el nombre del archivo de certificado.

    **MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*

 

 



