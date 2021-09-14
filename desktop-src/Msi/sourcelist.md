---
description: La propiedad SOURCELIST es una lista delimitada por punto y coma de rutas de acceso de origen de red o dirección URL al paquete de instalación de la aplicación.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propiedad SOURCELIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266063"
---
# <a name="sourcelist-property"></a>Propiedad SOURCELIST

La **propiedad SOURCELIST** es una lista delimitada por punto y coma de rutas de acceso de origen de red o dirección URL al paquete de instalación de la aplicación. Esta lista se anexa al final de la lista de origen existente de cada usuario para la aplicación. El instalador busca un origen enumerando la lista de rutas de acceso de origen y usa la primera ubicación accesible que encuentra. Solo este origen se puede usar para el resto de la instalación. Por lo tanto, cada ruta de acceso especificada en la lista de origen debe ser a una ubicación que tenga un origen completo para la aplicación. El árbol de directorios completo de cada ubicación de origen debe ser el mismo y debe incluir todos los archivos de origen necesarios, incluidos los gabinetes. Cada ubicación debe tener un .msi con el mismo nombre de archivo y código de producto.

## <a name="default-value"></a>Valor predeterminado

El instalador solo comprueba la **propiedad SOURCELIST** si el producto aún no se ha anunciado o instalado. En todos los demás casos, el instalador usa la lista de origen existente que se encuentra en el Registro.

## <a name="remarks"></a>Observaciones

Los orígenes agregados mediante la **propiedad SOURCELIST** se agregan directamente al final de la lista para cada tipo de origen y siempre vienen después del origen predeterminado especificado por la [**propiedad SourceDir.**](sourcedir.md)

Por Windows Installer, el número de orígenes de la **propiedad SOURCELIST** es ilimitado. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) se puede usar para agregar orígenes de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




