---
description: La tabla ComPlus contiene información necesaria para instalar aplicaciones COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabla de ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653025"
---
# <a name="complus-table"></a>Tabla de ComPlus

La tabla ComPlus contiene información necesaria para instalar aplicaciones COM+.

La tabla ComPlus tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| ExpType     | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Una clave externa en la primera columna de la [tabla de componentes](component-table.md). Este es el componente que contiene la aplicación COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Exporte las marcas usadas durante la generación del archivo. msi. Para obtener más información, vea la documentación de COM+ en el kit de desarrollo de software (SDK) de Microsoft Windows.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Vea la [acción RegisterComPlus](registercomplus-action.md) y la [acción UnregisterComPlus](unregistercomplus-action.md).

Vea [instalar una aplicación com+ con el Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



