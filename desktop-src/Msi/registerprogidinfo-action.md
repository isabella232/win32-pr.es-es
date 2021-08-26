---
description: La acción RegisterProgIdInfo administra el registro de información de OLE ProgId con el sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Acción RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cebf5ddb3bf8b9c98ebea0364b685016d343afa283b937400360f31bbcebd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912835"
---
# <a name="registerprogidinfo-action"></a>Acción RegisterProgIdInfo

La acción RegisterProgIdInfo administra el registro de información de OLE ProgId con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterProgIdInfo debe ir después de la acción [InstallFiles,](installfiles-action.md) la acción [UnregisterProgIdInfo,](unregisterprogidinfo-action.md) [la acción RegisterClassInfo](registerclassinfo-action.md) y [la acción RegisterExtensionInfo.](registerextensioninfo-action.md)

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencias, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterProgIdInfo debe ir después [de RegisterExtensionInfo en](registerextensioninfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa del programa registrado. |



 

## <a name="remarks"></a>Comentarios

La acción RegisterProgIdInfo registra toda la información de ProgId de los servidores especificados en la tabla [ProgId](progid-table.md) y para los que se ha seleccionado el servidor de clases o el servidor de extensiones correspondiente para instalarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de clases](class-table.md)
</dt> <dt>

[Tabla de extensiones](extension-table.md)
</dt> </dl>

 

 



