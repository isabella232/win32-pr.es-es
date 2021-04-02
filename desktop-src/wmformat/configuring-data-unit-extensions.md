---
title: Configuración de extensiones de unidades de datos
description: Configuración de extensiones de unidades de datos
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- flujos, configurar extensiones de unidad de datos
- secuencias, extensiones de unidad de datos
- extensiones de unidad de datos, configurar
- perfiles, extensiones de unidad de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789183"
---
# <a name="configuring-data-unit-extensions"></a>Configuración de extensiones de unidades de datos

Los ejemplos escritos en archivos ASF pueden contener información adicional aparte de los ejemplos de medios. Esta información se incluye con las extensiones de unidad de datos. Para obtener más información acerca de las extensiones de unidad de datos, consulte [extensiones de unidad de datos](data-unit-extensions.md).

Para usar las extensiones de unidad de datos, debe configurar la secuencia en el perfil para que las acepte. Para configurar una extensión de unidad de datos para una secuencia, realice los pasos siguientes.

1.  Obtenga un puntero a la interfaz [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) llamando al método **QueryInterface** de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).
2.  Llame a [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para registrar un tipo de extensión de unidad de datos para la secuencia.

Puede examinar todos los tipos de extensión de unidad de datos registrados actualmente para una secuencia llamando a [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) para recuperar el número de tipos de extensión de unidad de datos registrados. A continuación, puede recorrer todos los tipos mediante llamadas a [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) para cada uno.

A las extensiones de unidad de datos se les asigna un tamaño cuando se configuran para un flujo. Muchos sistemas de extensión de unidad de datos usan datos que tienen un tamaño constante (normalmente una estructura). Sin embargo, también puede configurar las extensiones de unidad de datos para que tengan un tamaño variable al establecer el tamaño en 0xFFFF. Cada extensión de unidad de datos asignada en el momento de la codificación puede tener cualquier tamaño entre 1 byte y 65534 bytes. Las extensiones de unidad de datos de tamaño variable también se denominan extensiones de unidad de datos dinámicos.

La ventaja de usar las extensiones de unidad de datos dinámicas es que puede adjuntar datos de extensión según sea necesario. Si define una extensión de unidad de datos con un tamaño establecido, cada muestra de la secuencia debe contener datos de extensión de ese tamaño, aunque no tenga datos para algunos ejemplos. Con las extensiones de unidad de datos dinámicos, puede omitir las extensiones de unidad de datos de algunos ejemplos, lo que ahorra espacio y reduce los requisitos de ancho de banda. Sin embargo, si las extensiones de unidad de datos son de tamaño variable, el objeto de lectura no puede comprobar los datos de la extensión recibida con respecto a un tamaño estático. Debe comprobar que los datos de la extensión que recibe son válidos, y no la distorsión malintencionada del flujo de bits.

Las extensiones de unidad de datos individuales deben establecerse en ejemplos mediante el método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Para obtener más información, consulte [configuración de las extensiones de unidad de datos](setting-data-unit-extensions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> </dl>

 

 




