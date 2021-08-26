---
title: Modificación de atributos con ADSI
description: Para modificar los valores de atributo, ADSI proporciona los métodos IADs.Put e IADs.PutEx. Estos métodos modifican los datos de la caché del lado cliente. Se debe llamar al método IADs.SetInfo para confirmar los cambios en el directorio.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modificación de atributos con ADSI
- ATRIBUTOS ADSI, Modificar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef82d6a3d4c486fcd1fca1f5cba7ae62f57e66e713ed84551a5a9372cdc86683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079965"
---
# <a name="modifying-attributes-with-adsi"></a>Modificación de atributos con ADSI

Para modificar los valores de atributo, ADSI proporciona los [**métodos IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) [**e IADs.PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Estos métodos modifican los datos de la caché del lado cliente. Se [**debe llamar al método IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.

> [!Note]  
> Cuando se confirman varios cambios de atributo en una sola llamada a [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), si no se puede modificar ningún atributo único, no se modificará ninguno de los atributos. Por ejemplo, si modifica los atributos [**sn**](/windows/desktop/ADSchema/a-sn) y [**givenName**](/windows/desktop/ADSchema/a-givenname) y borra el atributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) de un objeto de usuario sin llamadas posteriores al **método SetInfo,** los cambios se introducen al llamar a **SetInfo**. Si no se permiten una o varias de las modificaciones y, por tanto, no se pueden realizar, ninguna de las modificaciones colectivas realizadas en los atributos se introduce durante la llamada a **SetInfo**.

 

El [**método IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) toma un nombre de atributo y un parámetro variant. Use este método para establecer atributos que contienen valores únicos y varios.

El [**método IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) proporciona control sobre las operaciones en atributos con varios valores. Puede anexar, eliminar, actualizar y borrar los valores existentes. El **método IADs.PutEx** siempre espera una matriz variante de valores de atributo. Sin embargo, también puede usar este método para establecer un atributo con un solo valor.

El [**método IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa las operaciones especificadas por la [**enumeración ADS PROPERTY OPERATION \_ \_ \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)

 

 