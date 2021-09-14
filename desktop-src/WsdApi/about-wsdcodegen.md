---
description: Describe los archivos de entrada consumidos por WsdCodeGen y los archivos de salida generados por WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Acerca de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973708"
---
# <a name="about-wsdcodegen"></a>Acerca de WsdCodeGen

WsdCodeGen usa un archivo de configuración XML para determinar la ubicación de los metadatos del servicio. El archivo de configuración también se usa para definir nombres de interfaz, GUID de interfaz, nombres de clase, nombres de método y otros identificadores. Para obtener más información sobre este archivo, vea [Archivo de configuración de WsdCodeGen](wsdcodegen-configuration-file.md).

WsdCodeGen requiere dos tipos de archivos de entrada: un archivo de configuración XML y uno o varios archivos de descripción de servicio (archivos WSDL o XSD). WsdCodeGen procesa estos archivos de entrada y genera dos tipos de archivos de salida: archivos de interfaz y archivos de encabezado o origen.

## <a name="input-files"></a>Archivos de entrada



| Tipo                      | Descripción                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo de configuración        | Un archivo XML que indica la ubicación de los metadatos del servicio y define nombres de interfaz, GUID de interfaz, nombres de clase, nombres de método y otros identificadores. |
| Archivos de descripción del servicio | Uno o varios archivos WSDL o XSD que describen los servicios que se implementan en el dispositivo.                                                                           |



 

## <a name="output-files"></a>Archivos de resultados



| Tipo                        | Descripción                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivos de interfaz             | Un archivo IDL (lenguaje de definición de interfaz) que se puede usar con el compilador MIDL para generar un archivo de encabezado de interfaz. Los clientes de WSDAPI y los servicios WSDAPI pueden usar este archivo de interfaz.                                                                                                                                                           |
| Archivos de código fuente y encabezado de C++ | Archivos de C++ que describen el contrato de mensaje, el espacio de nombres y la información de tipos. Pueden contener código proxy o código auxiliar. El código proxy implementa la interfaz de un servicio y traduce las llamadas al método de servicio en operaciones de WSDAPI que realicen solicitudes de servicio. El código auxiliar traduce las solicitudes de servicio de WSDAPI en código que llama a métodos de servicio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Generador de código de Servicios web en dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[Uso de WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 



