---
title: Edición de atributos de metadatos
description: Edición de atributos de metadatos
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows SDK de formato multimedia, edición de atributos de metadatos
- Formato de sistemas avanzados (ASF), edición de atributos de metadatos
- ASF (formato de sistemas avanzados), edición de atributos de metadatos
- metadatos, edición de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973b787b37bbf9333a0adb218ab5db0e6f677521f1bfc9a0cdc1d5c37200e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586065"
---
# <a name="editing-metadata-attributes"></a>Edición de atributos de metadatos

La edición de atributos de metadatos es muy similar a la configuración de otros nuevos. En lugar de [**usar IWMHeaderInfo3::AddAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** es idéntico a **AddAttribute,** salvo que no se especifica un nombre de atributo y el número de índice es un parámetro de entrada en lugar de una salida.

Puede usar el número de flujo 0xFFFF especificar un atributo que se va a modificar mediante su índice global.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




