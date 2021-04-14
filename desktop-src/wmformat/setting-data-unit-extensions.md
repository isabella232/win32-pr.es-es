---
title: Configuración de las extensiones de unidad de datos
description: Configuración de las extensiones de unidad de datos
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- extensiones de unidad de datos, configuración
- secuencias, extensiones de unidad de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104533046"
---
# <a name="setting-data-unit-extensions"></a>Configuración de las extensiones de unidad de datos

Algunas secuencias están configuradas para usar las extensiones de unidad de datos para asociar datos complementarios a ejemplos individuales. Para obtener más información acerca de los ejemplos extendidos, consulte [extensiones de unidad de datos](data-unit-extensions.md).

La mayoría de los sistemas de extensión de unidad de datos requieren una extensión en cada ejemplo de la secuencia. Si no proporciona una extensión del tamaño correcto, el escritor rechazará el ejemplo.

Para agregar datos extendidos a un ejemplo, use el método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Puede obtener información sobre las extensiones de unidad de datos configuradas en una secuencia mediante los métodos [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) y [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de extensiones de unidades de datos**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




