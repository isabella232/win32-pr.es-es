---
description: La propiedad EXECUTEMODE especifica cómo el instalador ejecuta las actualizaciones del sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propiedad EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691094"
---
# <a name="executemode-property"></a>Propiedad EXECUTEMODE

La propiedad **EXECUTEMODE** especifica cómo el instalador ejecuta las actualizaciones del sistema. Esta propiedad puede ser útil cuando es necesario ejecutar una instalación sin cambiar realmente el sistema. La propiedad se puede establecer en None para deshabilitar las operaciones de actualización, como la instalación de archivos y valores del registro.

Esta propiedad puede tener uno de los dos valores siguientes. El instalador solo examina la primera letra del valor y no distingue entre mayúsculas y minúsculas.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>Ninguna
</dt> <dd>

No se realiza ningún cambio en el sistema. El instalador ejecuta la interfaz de usuario y, a continuación, consulta la base de datos.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Manuscrit
</dt> <dd>

Todos los cambios en el sistema se realizan a través de la ejecución del script. Este es el modo predeterminado.

</dd> </dl>

## <a name="default-value"></a>Valor predeterminado

Si no se define esta propiedad, el valor predeterminado del modo de ejecución es script.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




