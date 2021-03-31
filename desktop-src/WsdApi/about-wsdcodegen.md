---
description: Describe los archivos de entrada utilizados por WsdCodeGen y los archivos de salida generados por WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Acerca de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082444"
---
# <a name="about-wsdcodegen"></a>Acerca de WsdCodeGen

WsdCodeGen usa un archivo de configuración XML para determinar la ubicación de los metadatos del servicio. El archivo de configuración también se utiliza para definir los nombres de interfaz, los GUID de interfaz, los nombres de clase, los nombres de método y otros identificadores. Para obtener más información sobre este archivo, vea [archivo de configuración WsdCodeGen](wsdcodegen-configuration-file.md).

WsdCodeGen requiere dos tipos de archivos de entrada: un archivo de configuración XML y uno o más archivos de descripción de servicio (archivos WSDL o XSD). WsdCodeGen procesa estos archivos de entrada y genera dos tipos de archivos de salida: archivos de interfaz y archivos de encabezado/origen.

## <a name="input-files"></a>Archivos de entrada



| Tipo                      | Descripción                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo de configuración        | Archivo XML que indica la ubicación de los metadatos del servicio y define los nombres de interfaz, los GUID de interfaz, los nombres de clase, los nombres de método y otros identificadores. |
| Archivos de descripción de servicio | Uno o más archivos WSDL o XSD que describen los servicios que se van a implementar en el dispositivo.                                                                           |



 

## <a name="output-files"></a>Archivos de resultados



| Tipo                        | Descripción                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivos de interfaz             | Un archivo IDL (lenguaje de definición de interfaz) que se puede usar con el compilador MIDL para generar un archivo de encabezado de interfaz. Los clientes WSDAPI y los servicios WSDAPI pueden utilizar este archivo de interfaz.                                                                                                                                                           |
| Archivos de encabezado y código fuente de C++ | Archivos de C++ que describen el contrato de mensaje, el espacio de nombres y la información de tipo. Pueden contener código proxy o código auxiliar. El código proxy implementa la interfaz de un servicio y convierte las llamadas a métodos de servicio en operaciones de WSDAPI que realizan solicitudes de servicio. El código auxiliar traduce las solicitudes del servicio WSDAPI en el código que llama a los métodos de servicio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Generador de código de servicios web en dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[Usar WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 



