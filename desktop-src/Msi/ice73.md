---
description: ICE73 comprueba que el paquete no reutiliza códigos de paquete, códigos de actualización ni códigos de producto de los ejemplos del SDK Windows Installer. Los paquetes nunca deben volver a usar el paquete, la actualización o los códigos de producto de otro producto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074548"
---
# <a name="ice73"></a>ICE73

ICE73 comprueba que el paquete no reutiliza códigos de paquete, códigos de actualización ni códigos de producto de los ejemplos del SDK Windows Installer. Los paquetes nunca deben volver a usar el paquete, la actualización o los códigos de producto de otro producto.

## <a name="result"></a>Resultado

ICE73 genera una advertencia si el paquete del producto reutiliza un paquete o código de producto de un Windows SDK del instalador.

## <a name="example"></a>Ejemplo

ICE73 notifica los siguientes errores para el ejemplo que se muestra:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Los asteriscos ( ) del GUID representan el intervalo de GUID reservados para los paquetes posteriores \* \* \* \* Windows SDK del instalador.

 

Para corregir los errores, genere un nuevo GUID único para los códigos de producto y paquete del paquete. También necesitará un nuevo GUID único para el código de actualización del paquete.

[Secuencia de información de resumen](summary-information-stream.md) (parcial)



| Propiedad.       | Value                                  |
|----------------|----------------------------------------|
| PID \_ REVNUMBER | {000C1101-0000-0000-C000-00000000047} |



 

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad.                           | Value                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**UpgradeCode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de paquete](package-codes.md)
</dt> <dt>

[Códigos de producto](product-codes.md)
</dt> <dt>

[**Propiedad Resumen del número de revisión**](revision-number-summary.md)
</dt> <dt>

[**Propiedad UpgradeCode**](upgradecode.md)
</dt> <dt>

[**Propiedad ProductCode**](productcode.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



