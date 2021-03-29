---
description: Use los comandos MakeCert para crear certificados de prueba con las opciones disponibles con la versión 4,0 o posterior de Internet Explorer.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Uso de MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811234"
---
# <a name="using-makecert"></a>Uso de MakeCert

En los ejemplos siguientes se usan comandos [Makecert](makecert.md) para crear certificados de prueba mediante las opciones disponibles con Internet Explorer versión 4,0 o posterior.

-   Cree un certificado emitido por la raíz de prueba predeterminada. Guarde el certificado en un archivo.

    **Makecert** *MyNew. cer*

-   Cree un certificado emitido por la raíz de prueba predeterminada. Guárdelo en un almacén de certificados.

    **Makecert-SS** *MyNewStore*

-   Cree un certificado emitido por la raíz de prueba predeterminada. Cree un contenedor de claves y guarde el certificado en un almacén y en un archivo.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer*

-   Cree un certificado emitido por la raíz de prueba predeterminada. Cree un archivo de clave privada y guarde el certificado en un almacén y en un archivo.

    **Makecert-SV** *MyKeyFile* **-SS** *MyNewStore* *MyNew. cer*

-   Cree un certificado emitido por la raíz de prueba predeterminada. Cree un contenedor de claves, guarde el certificado en un almacén y un archivo, y haga que la clave privada se pueda exportar.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* *MyNew. cer* **-PE**

-   Cree un certificado mediante la raíz de prueba predeterminada. Guarde el certificado en un almacén. A continuación, cree otro certificado emitido por el certificado recién creado. Guarde el segundo certificado en otro almacén.

    **Makecert-SK** *MyNewKey* **-SS** *MyNewStore* **Makecert-is** *MyNewStore* **-SS** *AnotherStore*

-   Cree un certificado mediante la raíz de prueba predeterminada. Guarde el certificado en mi almacén. A continuación, cree otro certificado mediante el certificado recién creado. Si hay más de un certificado en el almacén MY, el certificado se debe identificar mediante su nombre común.

    **Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My Makecert-is My-in "XXZZYY"-SS** *AnotherStore*

-   Cree un certificado mediante la raíz de prueba predeterminada. Guarde el certificado en el almacén MY y en un archivo. A continuación, cree otro certificado mediante el certificado *MyNew* recién creado. Si hay más de un certificado en el almacén MY, identifique de forma única el primer certificado con el nombre de archivo del certificado.

    **Makecert-SK** *MyNewKey* **-n "CN = XXZZYY"-SS My** *MyNew. cer* **Makecert-is My-IC** *MyNew. cer* **-SS** *AnotherStore*

 

 



