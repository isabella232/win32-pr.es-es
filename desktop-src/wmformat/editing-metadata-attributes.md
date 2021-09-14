---
title: Editar atributos de metadatos
description: Editar atributos de metadatos
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows SDK de formato multimedia, edición de atributos de metadatos
- Formato de sistemas avanzados (ASF), edición de atributos de metadatos
- ASF (formato de sistemas avanzados), edición de atributos de metadatos
- metadatos, edición de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262196"
---
# <a name="editing-metadata-attributes"></a>Editar atributos de metadatos

La edición de atributos de metadatos es muy similar a la configuración de otros nuevos. En lugar de [**usar IWMHeaderInfo3::AddAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** es idéntico a **AddAttribute,** salvo que no se especifica un nombre de atributo y el número de índice es un parámetro de entrada en lugar de una salida.

Puede usar el número de secuencia 0xFFFF especificar un atributo que se va a modificar mediante su índice global.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




