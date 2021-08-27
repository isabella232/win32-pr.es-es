---
description: La propiedad EXECUTEMODE especifica cómo ejecuta el instalador las actualizaciones del sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: ExecuteMODE, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 750b6c3a20ab05388fcd6926463dde8259440bd6087306b1bf0cc1a6c387cd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082875"
---
# <a name="executemode-property"></a>ExecuteMODE, propiedad

La **propiedad EXECUTEMODE** especifica cómo ejecuta el instalador las actualizaciones del sistema. Esta propiedad puede ser útil cuando es necesario ejecutar una instalación sin cambiar realmente el sistema. La propiedad se puede establecer en None para deshabilitar operaciones de actualización, como la instalación de archivos y valores del Registro.

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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




