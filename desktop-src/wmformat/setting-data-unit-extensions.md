---
title: Establecer extensiones de unidad de datos
description: Establecer extensiones de unidad de datos
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Formato de sistemas avanzados (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- extensiones de unidad de datos, configuración
- streams,extensiones de unidad de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570205"
---
# <a name="setting-data-unit-extensions"></a>Establecer extensiones de unidad de datos

Algunas secuencias están configuradas para usar extensiones de unidad de datos para asociar datos adicionales a muestras individuales. Para obtener más información sobre los ejemplos [extendidos,](data-unit-extensions.md)vea Extensiones de unidad de datos .

La mayoría de los sistemas de extensión de unidad de datos requieren una extensión en cada ejemplo del flujo. Si no proporciona una extensión del tamaño correcto, el escritor rechazará el ejemplo.

Para agregar datos extendidos a un ejemplo, use el [**método INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Puede obtener información sobre las extensiones de unidad de datos configuradas en una secuencia mediante los métodos [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2::GetDataUnitExtension.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de extensiones de unidades de datos**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




