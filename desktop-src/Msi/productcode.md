---
description: La propiedad ProductCode es un identificador único para la versión de producto determinada, representada como un GUID de cadena, por ejemplo, \# &0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propiedad ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a77ba270075b214d5eee2ee804c6849a2ef71561610ee60ae3eb4941e43465c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753915"
---
# <a name="productcode-property"></a>Propiedad ProductCode

La **propiedad ProductCode** es un identificador único para la versión de producto determinada, representada como [un GUID](guid.md)de cadena , por ejemplo " {12345678-1234-1234-1234-123456789012} ". Las letras usadas en este GUID deben estar en mayúsculas. Este identificador debe variar para diferentes versiones e idiomas.

Una actualización de producto que actualice un producto a un producto completamente nuevo también debe cambiar el código del producto. Las versiones de 32 y 64 bits del paquete de una aplicación deben tener asignados códigos de producto diferentes.

ProductCode **se** anuncia como una propiedad de producto y es el método principal para especificar el producto. Esta propiedad es REQUIRED.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




