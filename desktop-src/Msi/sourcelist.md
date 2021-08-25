---
description: La propiedad SOURCELIST es una lista delimitada por punto y coma de rutas de acceso de origen de red o dirección URL al paquete de instalación de la aplicación.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propiedad SOURCELIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd0ab879d55481f71c663e4375a305232be576d0c923f67fa419530012d1ce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893755"
---
# <a name="sourcelist-property"></a>Propiedad SOURCELIST

La **propiedad SOURCELIST** es una lista delimitada por punto y coma de rutas de acceso de origen de red o dirección URL al paquete de instalación de la aplicación. Esta lista se anexa al final de la lista de origen existente de cada usuario para la aplicación. El instalador busca un origen enumerando la lista de rutas de acceso de origen y usa la primera ubicación accesible que encuentra. Solo este origen se puede usar durante el resto de la instalación. Por lo tanto, cada ruta de acceso especificada en la lista de origen debe estar en una ubicación que tenga un origen completo para la aplicación. El árbol de directorios completo de cada ubicación de origen debe ser el mismo y debe incluir todos los archivos de origen necesarios, incluidos los archivadores. Cada ubicación debe tener un archivo .msi con el mismo nombre de archivo y código de producto.

## <a name="default-value"></a>Valor predeterminado

El instalador solo comprueba la **propiedad SOURCELIST** si el producto aún no se ha anunciado o instalado. En todos los demás casos, el instalador usa la lista de origen existente que se encuentra en el Registro.

## <a name="remarks"></a>Comentarios

Los orígenes agregados mediante la **propiedad SOURCELIST** se agregan directamente al final de la lista para cada tipo de origen y siempre vienen después del origen predeterminado especificado por la [**propiedad SourceDir.**](sourcedir.md)

Para Windows instalador, el número de orígenes de la **propiedad SOURCELIST** es ilimitado. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) se puede usar para agregar orígenes de red.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




