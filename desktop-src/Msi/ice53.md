---
description: ICE53 comprueba las entradas de la tabla del registro que escriben información privada del instalador o valores de directiva en el registro del sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652921"
---
# <a name="ice53"></a>ICE53

ICE53 comprueba las entradas de la tabla del registro que escriben información privada del instalador o valores de directiva en el registro del sistema.

## <a name="result"></a>Resultado

ICE53 publica una advertencia si la tabla del registro especifica escribir información interna o de directiva en el registro.

## <a name="example"></a>Ejemplo

ICE53 envía la siguiente advertencia para el ejemplo que se muestra.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Tabla del registro](registry-table.md) (parcial)



| Registro             | Root         | Clave                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Software** \\ de **Directivas** \\ de **Microsoft** \\ **Windows** \\ **Instalador** \\ de **DisableRollback**<br/> |



 

La fila de la tabla del registro ' Registry1 ' escribe un valor de directiva del sistema en el registro que afecta a la instalación de todos los paquetes. Dependiendo del paquete, es posible deshabilitar la reversión de este paquete por sí solo si se establece la propiedad [**DISABLEROLLBACK**](-disablerollback.md) en la [tabla de propiedades](property-table.md). Consulte [reversión de instalación](rollback-installation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




