---
description: La propiedad ProductCode es un identificador único de la versión de producto determinada, representada como un GUID de cadena, por ejemplo &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propiedad ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680661"
---
# <a name="productcode-property"></a>Propiedad ProductCode

La propiedad **ProductCode** es un identificador único de la versión de producto determinada, representada como un [GUID](guid.md)de cadena, por ejemplo " {12345678-1234-1234-1234-123456789012} ". Las letras usadas en este GUID deben estar en mayúsculas. Este identificador debe variar en diferentes versiones e idiomas.

Una actualización de producto que actualice un producto en un producto completamente nuevo también debe cambiar el código de producto. Las versiones de 32 bits y 64 bits del paquete de una aplicación deben tener asignados distintos códigos de producto.

El **ProductCode** se anuncia como una propiedad del producto y es el método principal para especificar el producto. Esta propiedad es obligatoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




