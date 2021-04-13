---
title: Registro binario centralizado
description: El registro binario centralizado es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bc7bdc6f7a5fce78ff66e58b4c50eac36be3f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358916"
---
# <a name="centralized-binary-logging"></a>Registro binario centralizado

El registro binario centralizado es un tipo de registro del lado servidor que se puede habilitar en la sesión del servidor. El registro binario centralizado funciona como una forma centralizada de registro para todos los grupos de direcciones URL creados en la sesión de servidor y permite que todos los grupos de direcciones URL de la sesión del servidor envíen datos de registro binarios sin formato a un solo archivo de registro. Este tipo de registro solo se puede habilitar en la sesión del servidor; no se puede habilitar en el grupo de direcciones URL.

## <a name="when-to-use-centralized-binary-logging"></a>Cuándo usar el registro binario centralizado

Cuando la sesión de servidor tiene varios grupos de direcciones URL debajo, el proceso de creación de cientos de archivos de registro con formato para los grupos de direcciones URL individuales y la escritura de los datos de registro en un disco puede consumir rápidamente recursos valiosos de CPU y memoria, con lo que se crean problemas de rendimiento y escalabilidad. El registro binario centralizado reduce la cantidad de recursos del sistema que se usan para el registro, al mismo tiempo que proporciona datos de registro detallados para las organizaciones que lo requieren.

El registro binario centralizado es una propiedad de sesión de servidor que, cuando está habilitada, configura el registro de todos los grupos de direcciones URL en la sesión de servidor. Cuando el registro binario centralizado está habilitado, los datos no se pueden grabar ni formatear para grupos de direcciones URL individuales. El archivo de registro de registro binario centralizado tiene una extensión de nombre de archivo de registro binario de Internet (. IBL). Esta extensión de nombre de archivo garantiza que las utilidades de texto no intenten abrir y leer el archivo de registro de registro binario central.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Extraer datos del archivo de registro binario centralizado

Los pasos siguientes se realizan para extraer datos de un archivo de registro sin procesar:

-   Cree una herramienta que busque y extraiga los datos que desee del archivo sin formato y los convierta en texto con formato. Puede ver las descripciones de los archivos de encabezado y de archivo de registro en el kit de desarrollo de software de IIS 6,0 en MSDN.
-   Use la herramienta log parser para extraer datos del archivo sin formato. La herramienta de análisis de registros y la documentación de usuario correspondiente se incluyen en las herramientas del kit de recursos de IIS 6,0.

## <a name="centralized-binary-logging-file-format"></a>Formato de archivo de registro binario centralizado

El archivo de registro de registro binario centralizado sin formato se compone de registros de longitud fija o registros de índice que contienen identificadores de cadena. Los registros de índice aparecen porque, en un intento de registrar tanta información como sea posible, los campos de cadena de longitud variable se reemplazan por los identificadores numéricos (índices) que asignan la cadena de longitud variable al identificador registrado.

El archivo de registro sin procesar no es legible y no se puede leer con la mayoría de los analizadores de registro disponibles. Para extraer datos de un archivo de registro sin procesar, puede crear una herramienta que busque y extraiga los datos y, a continuación, los convierta en texto con formato.

Para obtener más información, vea el registro de datos [binarios centralizados](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) en Microsoft TechNet.

 

 