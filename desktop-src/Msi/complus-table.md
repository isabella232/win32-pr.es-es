---
description: La tabla Complus contiene la información necesaria para instalar aplicaciones COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Complus Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77885688226689e5d81e074b1a9a28ef3801aaeba5febf51165377ac9ad9e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144976"
---
# <a name="complus-table"></a>Complus Table

La tabla Complus contiene la información necesaria para instalar aplicaciones COM+.

La tabla Complus tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| ExpType     | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md). Este es el componente que contiene la aplicación COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Exportar marcas usadas durante la generación del .msi archivo. Para obtener más información, consulte la documentación de COM+ en Microsoft Windows Software Development Kit (SDK) de Microsoft.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Vea la [acción RegisterComPlus y](registercomplus-action.md) [la acción UnregisterComPlus](unregistercomplus-action.md).

Vea Installing a COM+ Application with the Windows Installer (Instalación de una [aplicación COM+ con Windows instalador).](installing-a-com--application-with-the-windows-installer.md)

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



