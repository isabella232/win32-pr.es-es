---
description: La tabla Complus contiene la información necesaria para instalar aplicaciones COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Complus Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158850"
---
# <a name="complus-table"></a>Complus Table

La tabla Complus contiene la información necesaria para instalar aplicaciones COM+.

La tabla Complus tiene las siguientes columnas.



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

Exportar marcas usadas durante la generación del .msi archivo. Para obtener más información, consulte la documentación de COM+ en Microsoft Windows Software Development Kit (SDK).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Vea la [acción RegisterComPlus y](registercomplus-action.md) [la acción UnregisterComPlus](unregistercomplus-action.md).

Consulte [Instalación de una aplicación COM+ con Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



