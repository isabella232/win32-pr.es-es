---
title: Editar atributos de metadatos
description: Editar atributos de metadatos
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- SDK de Windows Media Format, Editar atributos de metadatos
- Advanced Systems Format (ASF), Editar atributos de metadatos
- ASF (formato de sistemas avanzados), Editar atributos de metadatos
- metadatos, Editar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420314"
---
# <a name="editing-metadata-attributes"></a>Editar atributos de metadatos

La edición de atributos de metadatos es muy similar a la configuración de otras nuevas. En lugar de usar [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3:: ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** es idéntico a **AddAttribute** , salvo que no se especifica un nombre de atributo y el número de índice es un parámetro de entrada en lugar de un resultado.

Puede usar el número de secuencia 0xFFFF para especificar un atributo que se va a modificar mediante su índice global.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




