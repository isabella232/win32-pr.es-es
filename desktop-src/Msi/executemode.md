---
description: La propiedad EXECUTEMODE especifica cómo el instalador ejecuta las actualizaciones del sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propiedad EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158428"
---
# <a name="executemode-property"></a>Propiedad EXECUTEMODE

La **propiedad EXECUTEMODE** especifica cómo el instalador ejecuta las actualizaciones del sistema. Esta propiedad puede ser útil cuando es necesario ejecutar una instalación sin cambiar realmente el sistema. La propiedad se puede establecer en None para deshabilitar las operaciones de actualización, como la instalación de archivos y valores del Registro.

Esta propiedad puede tener uno de los dos valores siguientes. El instalador solo examina la primera letra del valor y no tiene en cuenta las mayúsculas y minúsculas.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>Ninguno
</dt> <dd>

No se realiza ningún cambio en el sistema. El instalador ejecuta la interfaz de usuario y, a continuación, consulta la base de datos.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Guión
</dt> <dd>

Todos los cambios realizados en el sistema se realizan mediante la ejecución de scripts. Este es el modo predeterminado.

</dd> </dl>

## <a name="default-value"></a>Valor predeterminado

Si no se define esta propiedad, el modo de ejecución tiene como valor predeterminado Script.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




