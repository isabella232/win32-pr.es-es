---
description: ICE99 comprueba que ningún nombre de propiedad especificado en la tabla del directorio duplica un nombre reservado para el uso público o privado del Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814411"
---
# <a name="ice99"></a>ICE99

ICE99 comprueba que ningún nombre de propiedad especificado en la tabla del [directorio](directory-table.md) duplica un nombre reservado para el uso público o privado del Windows Installer.

## <a name="result"></a>Resultado

ICE99 expone el siguiente error.



| Error ICE99                                                                                                      | Descripción                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| El nombre del directorio: \[ 1 \] es el mismo que el de una de las propiedades públicas de MSI y puede producir efectos secundarios imprevistos. | El valor de la columna Directory de la tabla [Directory](directory-table.md) duplica un nombre de propiedad reservado por el Windows Installer. |



 

## <a name="example"></a>Ejemplo

ICE99 notifica el siguiente error para el ejemplo:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Directorio](directory-table.md) (parcial)



| Directorio        | Directorio \_ primario | DefaultDir |
|------------------|-------------------|------------|
| CustomActionData |                   |            |



 

Para corregir esta advertencia, debe cambiar el nombre de CustomActionData.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> <dt>

[Tabla de directorio](directory-table.md)
</dt> <dt>

[No se admite en Windows Installer 3,0 y versiones anteriores](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



