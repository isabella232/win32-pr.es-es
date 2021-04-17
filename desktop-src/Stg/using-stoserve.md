---
title: Usar StoServe
description: StoServe es un archivo DLL que está diseñado principalmente como un servidor COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665863"
---
# <a name="using-stoserve"></a>Usar StoServe

**StoServe** es un archivo DLL que está diseñado principalmente como un servidor com. Aunque se puede cargar implícitamente vinculando a su asociado. Archivo LIB, normalmente se utiliza después de una llamada LoadLibrary explícita, normalmente desde dentro de la función COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe** es un servidor de proceso de registro automático.

Para usar **StoServe**, un programa cliente no necesita incluir StoServe. H o vínculo a STOSERVE. Obj. Un cliente COM de **StoServe** obtiene el acceso exclusivamente a través de los servicios de CLSID y com de su objeto. En el caso de **StoServe**, ese CLSID es CLSID \_ DllPaper (definido en el archivo PAPGUIDS. H en el \\ directorio del mismo nivel. En el ejemplo de código [StoClien](structured-storage-client-sample--stoclien-.md) se muestra cómo el cliente obtiene este acceso.

El archivo make que compila este ejemplo registra automáticamente el servidor en el registro. Puede iniciar manualmente su propio registro mediante la emisión del comando siguiente en el símbolo del sistema en el directorio **StoServe** :

 **registro** de NMAKE

Se supone que tiene un entorno de compilación configurado. Si no es así, también puede invocar directamente el comando REGISTER.EXE en el símbolo del sistema mientras se encuentra en el directorio **StoServe**

**..\\ registrar \\register.exe** **stoserve.dll**

Estos comandos de registro requieren una compilación anterior del ejemplo de registro en esta serie, así como una compilación anterior de STOSERVE.DLL.

En esta serie, los archivos make usan la utilidad REGISTER.EXE del ejemplo REGISTER. Las versiones recientes del kit de desarrollo de software (SDK) de la plataforma y Visual C++ incluyen una utilidad, REGSVR32.EXE, que se puede usar de forma similar para registrar servidores en proceso y calcular las referencias de los archivos dll.

**StoServe** usa muchas de las clases de utilidad y los servicios proporcionados por apputil. Para obtener más detalles sobre APPUTIL, estudie el código fuente de la biblioteca de APPUTIL en el directorio del APPUTIL relacionado y APPUTIL.HTM en el directorio principal del tutorial.

 

 