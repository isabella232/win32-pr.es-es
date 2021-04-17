---
description: La propiedad SOURCELIST es una lista delimitada por signos de punto y coma de rutas de acceso de origen de red o URL al paquete de instalación de la aplicación.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propiedad SOURCELIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653369"
---
# <a name="sourcelist-property"></a>Propiedad SOURCELIST

La propiedad **SourceList** es una lista delimitada por signos de punto y coma de rutas de acceso de origen de red o URL al paquete de instalación de la aplicación. Esta lista se anexa al final de la lista de origen existente de cada usuario de la aplicación. El instalador busca un origen enumerando la lista de rutas de acceso de origen y utiliza la primera ubicación accesible que encuentra. Solo se puede usar este origen para el resto de la instalación. Por lo tanto, cada ruta de acceso especificada en la lista de origen debe ser a una ubicación que tenga un origen completo para la aplicación. Todo el árbol de directorios en cada ubicación de origen debe ser el mismo y debe incluir todos los archivos de origen necesarios, incluidos los contenedores. Cada ubicación debe tener un archivo. msi con el mismo nombre de archivo y el mismo código de producto.

## <a name="default-value"></a>Valor predeterminado

El instalador solo comprueba la propiedad **SourceList** si el producto aún no se ha anunciado o instalado. En todos los demás casos, el instalador usa la lista de orígenes existente que se encuentra en el registro.

## <a name="remarks"></a>Observaciones

Los orígenes agregados mediante la propiedad **SourceList** se agregan directamente al final de la lista para cada tipo de origen y siempre van después del origen predeterminado especificado por la propiedad [**SourceDir**](sourcedir.md) .

Por Windows Installer el número de orígenes de la propiedad **SourceList** es ilimitado. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) se puede usar para agregar orígenes de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




