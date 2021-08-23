---
description: ICE99 comprueba que ningún nombre de propiedad especificado en la tabla Directorio duplica un nombre reservado para el uso público o privado del instalador de Windows.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315275"
---
# <a name="ice99"></a>ICE99

ICE99 comprueba que ningún nombre de propiedad especificado en la tabla [Directory](directory-table.md) duplica un nombre reservado para el uso público o privado del instalador de Windows.

## <a name="result"></a>Resultado

ICE99 publica el siguiente error.



| Error ICE99                                                                                                      | Descripción                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| El nombre del directorio: 1 es el mismo que una de las propiedades públicas de MSI y puede producir efectos secundarios \[ \] imprevistos. | El valor de la columna Directorio de la [tabla Directorio](directory-table.md) duplica un nombre de propiedad reservado por Windows Installer. |



 

## <a name="example"></a>Ejemplo

ICE99 notifica el siguiente error para el ejemplo:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Directorio](directory-table.md) (parcial)



| Directorio        | Elemento primario \_ del directorio | DefaultDir |
|------------------|-------------------|------------|
| Customactiondata |                   |            |



 

Para corregir esta advertencia, debe cambiar el nombre de CustomActionData.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> <dt>

[Tabla de directorios](directory-table.md)
</dt> <dt>

[No se admite en Windows Installer 3.0 y versiones anteriores](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



