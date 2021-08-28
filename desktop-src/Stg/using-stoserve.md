---
title: Uso de StoServe
description: StoServe es un archivo DLL diseñado principalmente como servidor COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3a220f03e17892b02a94c1e76bafc4a869c0922973c7277589627d233175a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034755"
---
# <a name="using-stoserve"></a>Uso de StoServe

**StoServe** es un archivo DLL diseñado principalmente como servidor COM. Aunque se puede cargar implícitamente mediante la vinculación a su asociado. Archivo LIB, normalmente se usa después de una llamada loadLibrary explícita, normalmente desde la función COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe** es un servidor en proceso de registro propio.

Para usar **StoServe,** un programa cliente no necesita incluir STOSERVE. H o vínculo a STOSERVE. Lib. Un cliente COM de **StoServe** obtiene acceso únicamente a través de los servicios CLSID y COM de su objeto. Para **StoServe**, ese CLSID es CLSID \_ DllPaper (definido en el archivo PAPGUIDS. H en el \\ directorio relacionado de INC). El [ejemplo de código StoClien](structured-storage-client-sample--stoclien-.md) muestra cómo el cliente obtiene este acceso.

El archivo Make que compila este ejemplo registra automáticamente el servidor en el registro. Puede iniciar manualmente su registro propio mediante la emisión del siguiente comando en el símbolo del sistema en el **directorio StoServe:**

**registro nmake** 

Se supone que tiene un entorno de compilación configurado. Si no es así, también puede invocar directamente el REGISTER.EXE en el símbolo del sistema mientras se encuentra en el **directorio StoServe.**

**..\\ registro \\register.exe** **stoserve.dll**

Estos comandos de registro requieren una compilación anterior del ejemplo REGISTER de esta serie, así como una compilación anterior de STOSERVE.DLL.

En esta serie, los archivos make usan la utilidad REGISTER.EXE del ejemplo REGISTER. Las versiones recientes de Platform Software Development Kit (SDK) y Visual C++ incluyen una utilidad, REGSVR32.EXE, que se puede usar de forma similar para registrar servidores en proceso y serializar archivos DLL.

**StoServe** usa muchas de las clases y servicios de utilidad proporcionados por APPUTIL. Para obtener más información sobre APPUTIL, consulte el código fuente de la biblioteca APPUTIL en el directorio APPUTIL relacionado y APPUTIL.HTM en el directorio principal del tutorial.

 

 