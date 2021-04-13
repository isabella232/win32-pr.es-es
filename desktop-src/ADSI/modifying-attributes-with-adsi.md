---
title: Modificar atributos con ADSI
description: Para modificar los valores de atributo, ADSI proporciona los métodos IADs. put y IADs. PutEx. Estos métodos modifican los datos en la memoria caché del lado cliente. Se debe llamar al método IADs. SetInfo para confirmar los cambios en el directorio.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modificar atributos con ADSI
- Atributos ADSI, modificar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421410"
---
# <a name="modifying-attributes-with-adsi"></a>Modificar atributos con ADSI

Para modificar los valores de atributo, ADSI proporciona los métodos [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Estos métodos modifican los datos en la memoria caché del lado cliente. Se debe llamar al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.

> [!Note]  
> Cuando se confirman varios cambios de atributo en una única llamada a [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), si no se puede modificar ningún atributo único, no se modificará ninguno de los atributos. Por ejemplo, si modifica los atributos [**SN**](/windows/desktop/ADSchema/a-sn) y [**givenName**](/windows/desktop/ADSchema/a-givenname) y borra el atributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) de un objeto User sin ninguna llamada subsiguiente al método **SetInfo** , los cambios se especifican al llamar a **SetInfo**. Si una o varias de las modificaciones no se permiten y, por lo tanto, no se pueden realizar, ninguna de las modificaciones colectivas realizadas en los atributos se especifican durante la llamada a **SetInfo**.

 

El método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) toma un nombre de atributo y un parámetro Variant. Use este método para establecer los atributos que contienen valores únicos y múltiples.

El método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) proporciona control sobre las operaciones en atributos con varios valores. Puede anexar, eliminar, actualizar y borrar valores existentes. El método **IADs. PutEx** siempre espera una matriz de valores de atributo Variant. Sin embargo, puede utilizar este método para establecer un atributo con un solo valor.

El método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa las operaciones especificadas por la enumeración de la enumeración de la operación de la [**\_ propiedad \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .

 

 