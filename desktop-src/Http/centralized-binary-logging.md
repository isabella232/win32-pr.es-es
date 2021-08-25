---
title: Registro binario centralizado
description: El registro binario centralizado es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2006270a6bdb2b06748214bff6170b369de791456577caeb62a9abc4b625bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047575"
---
# <a name="centralized-binary-logging"></a>Registro binario centralizado

El registro binario centralizado es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor. El registro binario centralizado funciona como una forma centralizada de registro para todos los grupos de direcciones URL creados en la sesión del servidor y permite que todos los grupos de direcciones URL de la sesión del servidor envíen datos de registro binarios sin formato a un único archivo de registro. Este tipo de registro solo se puede habilitar en la sesión de servidor; no se puede habilitar en el grupo de direcciones URL.

## <a name="when-to-use-centralized-binary-logging"></a>Cuándo usar el registro binario centralizado

Cuando la sesión del servidor tiene numerosos grupos de direcciones URL, el proceso de crear cientos de archivos de registro con formato para grupos de direcciones URL individuales y escribir los datos de registro en un disco puede consumir rápidamente valiosos recursos de CPU y memoria, lo que crea problemas de rendimiento y escalabilidad. El registro binario centralizado minimiza la cantidad de recursos del sistema que se usan para el registro y, al mismo tiempo, proporciona datos de registro detallados para las organizaciones que lo requieren.

El registro binario centralizado es una propiedad de sesión de servidor que, cuando está habilitada, configura el registro de todos los grupos de direcciones URL en la sesión del servidor. Cuando el registro binario centralizado está habilitado, los datos no se pueden registrar ni formatear para grupos de direcciones URL individuales. El archivo de registro binario centralizado tiene una extensión de nombre de archivo de registro binario de Internet (.ibl). Esta extensión de nombre de archivo garantiza que las utilidades de texto no intenten abrir y leer el archivo de registro binario central.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Extraer datos del archivo de registro binario centralizado

Los pasos siguientes se realizan para extraer datos de un archivo de registro sin formato:

-   Cree una herramienta que busque y extraiga los datos que desee del archivo sin formato y convierta los datos en texto con formato. Puede ver un archivo de encabezado y descripciones de formato de archivo de registro en el Kit de desarrollo de software de IIS 6.0 en MSDN.
-   Use la herramienta Log Parser para extraer datos del archivo sin formato. La herramienta Log Parser y su documentación de usuario que lo acompaña se incluyen en las herramientas del Kit de recursos de IIS 6.0.

## <a name="centralized-binary-logging-file-format"></a>Formato de archivo de registro binario centralizado

El archivo de registro binario centralizado sin procesar se conste de registros de longitud fija o registros de índice que contienen identificadores de cadena. Los registros de índice aparecen porque, en un esfuerzo por registrar tanta información como sea posible, los campos de cadena de longitud variable se reemplazan por identificadores numéricos (índices) que asignan la cadena de longitud variable al identificador registrado.

El archivo de registro sin formato no es legible y no se puede leer con la mayoría de los analizadores de registros disponibles. Para extraer datos de un archivo de registro sin formato, puede crear una herramienta que busque y extraiga los datos y, a continuación, los convierta en texto con formato.

Para obtener más información, [vea Registro binario centralizado](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) en Microsoft TechNet.

 

 