---
title: Configuración de extensiones de unidades de datos
description: Configuración de extensiones de unidades de datos
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- streams,configuring data unit extensions
- streams,extensiones de unidad de datos
- extensiones de unidad de datos, configurar
- perfiles, extensiones de unidad de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466497"
---
# <a name="configuring-data-unit-extensions"></a>Configuración de extensiones de unidades de datos

Los ejemplos escritos en archivos ASF pueden contener información adicional aparte de los propios ejemplos multimedia. Esta información se incluye mediante extensiones de unidad de datos. Para obtener más información sobre las extensiones de unidad de datos, vea [Extensiones de unidad de datos](data-unit-extensions.md).

Para usar extensiones de unidad de datos, debe configurar la secuencia en el perfil para que las acepte. Para configurar una extensión de unidad de datos para un flujo, realice los pasos siguientes.

1.  Obtenga un puntero a la [**interfaz IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) llamando al **método QueryInterface** [**de IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).
2.  Llame [**a IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para registrar un tipo de extensión de unidad de datos para la secuencia.

Puede examinar todos los tipos de extensión de unidad de datos registrados actualmente para una secuencia llamando a [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) para recuperar el número de tipos de extensión de unidad de datos registrados. A continuación, puede recorrer en bucle todos los tipos mediante llamadas a [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) para cada uno.

A las extensiones de unidad de datos se les asigna un tamaño cuando se configuran para una secuencia. Muchos sistemas de extensión de unidades de datos usan datos que tienen un tamaño constante (normalmente una estructura). Sin embargo, también puede configurar las extensiones de unidad de datos para que sean de tamaño variable estableciendo el tamaño en 0xFFFF. Cada extensión de unidad de datos asignada en tiempo de codificación puede tener cualquier tamaño entre 1 byte y 65534 bytes. Las extensiones de unidad de datos de tamaño variable también se denominan extensiones de unidad de datos dinámicas.

La ventaja de usar extensiones de unidad de datos dinámicas es que puede adjuntar datos de extensión según sea necesario. Si define una extensión de unidad de datos con un tamaño establecido, cada ejemplo de la secuencia debe contener datos de extensión de ese tamaño, incluso si no tiene datos para algunos ejemplos. Con las extensiones de unidad de datos dinámicas, puede omitir las extensiones de unidad de datos de algunos ejemplos, lo que ahorra espacio y reduce los requisitos de ancho de banda. Sin embargo, si las extensiones de unidad de datos tienen un tamaño variable, el objeto de lectura no puede comprobar los datos de extensión recibidos con un tamaño estático. Debe comprobar que los datos de extensión que recibe son válidos y no la distorsión malintencionada de la secuencia de bits.

Las extensiones de unidad de datos individuales deben establecerse en ejemplos mediante el [**método INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Para obtener más información, vea [Establecer extensiones de unidad de datos](setting-data-unit-extensions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




