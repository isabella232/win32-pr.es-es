---
description: Los usuarios y las aplicaciones con privilegios administrativos pueden recuperar y modificar la información de red, dirección URL y lista de orígenes multimedia para Windows Installer y revisiones en el sistema.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Administración de orígenes de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7555bc9595ba10d9ce569c15c2a8138a05348e503d86a025f0cfe1783843fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013073"
---
# <a name="managing-installation-sources"></a>Administración de orígenes de instalación

Los usuarios y las aplicaciones con privilegios administrativos pueden recuperar y modificar la información de red, dirección URL y lista de orígenes multimedia para Windows Installer y revisiones en el sistema.

**Windows Installer 2.0:** No se admite. Los administradores no pueden leer, reordenar ni reemplazar las entradas de la lista de origen y no pueden modificar ni recuperar las propiedades de la lista de origen. Es posible administrar orígenes de red, pero no orígenes de direcciones URL ni multimedia. Los administradores solo pueden administrar listas de origen para aplicaciones por máquina o aplicaciones instaladas por usuario para el usuario actual. Esto impide que los administradores que usan versiones anteriores a Windows Installer versión 3.0 puedan administrar la información de la lista de origen para todos los usuarios del sistema.

**Windows Installer 3.0 y versiones posteriores:** Los usuarios y las aplicaciones que tienen privilegios de administrador pueden recuperar y modificar la información de la lista de origen de las aplicaciones y revisiones de Windows Installer instaladas en el sistema para todos los usuarios. Las funciones de lista de origen se pueden usar para administrar listas de origen y propiedades de lista de origen para orígenes de red, direcciones URL y medios. El instalador puede reordenar las listas de origen de un proceso externo.

Los usuarios y aplicaciones que tienen privilegios administrativos pueden leer y modificar los siguientes tipos de información de la lista de origen:

-   Listas de origen para aplicaciones y revisiones instaladas para todos los usuarios del sistema.
-   Listas de origen para los orígenes de revisión que existen aparte de los orígenes de la aplicación.
-   Listas de origen para los orígenes de direcciones URL y medios que existen aparte de los orígenes de red.
-   Propiedades de lista de origen [**como MEDIAPACKAGEPATH,**](mediapackagepath.md) [**DiskPrompt,**](diskprompt.md) **LastUsedSource**, **LastUsedType** y **PackageName**.

Las funciones de listas de origen pueden limitar el ámbito de las listas de origen encontradas especificando el contexto de instalación y el contexto de usuario. Hay tres contextos de instalación posibles: por usuario (no administrado), por equipo y por usuario administrado. El contexto de usuario puede ser un usuario determinado o todos los usuarios del sistema.

Los usuarios que no son administradores no pueden modificar la lista de origen de una instancia de una aplicación o revisión que existe en el contexto por usuario (administrado o no administrado) de otro usuario. Los usuarios que no son administradores pueden modificar las listas de origen de una instancia de una aplicación o revisión instaladas en los contextos siguientes:

-   Su propio contexto por usuario (no administrado).
-   El contexto de la máquina, pero solo si las directivas [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)y [AlwaysInstallElevated](alwaysinstallelevated.md) les permite buscar una aplicación o un origen de revisión.
-   Su propio contexto administrado por usuario, pero solo si las directivas [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)y [AlwaysInstallElevated](alwaysinstallelevated.md) les permiten buscar una aplicación o un origen de revisión.

Los administradores pueden modificar cualquier lista de origen que un usuario que no sea administrador pueda modificar. Además, los administradores y las aplicaciones que tienen privilegios administrativos pueden modificar las listas de origen de una aplicación o revisión instaladas en los contextos siguientes:

-   Contexto por máquina.
-   Su propio contexto administrado por usuario (no administrado) o por usuario.
-   Contexto administrado por usuario de otro usuario.

> [!Note]  
> Los usuarios y las aplicaciones que tienen privilegios administrativos no pueden modificar la lista de origen de una instancia de una aplicación o revisión instalada en el contexto por usuario (no administrado) de otro usuario.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Administración de orígenes de redes y direcciones URL para productos y revisiones

Use la [**función MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para agregar o reordenar la lista de orígenes de red y dirección URL de una aplicación o revisión en un contexto determinado. Use el *parámetro dwContext* para especificar el contexto de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario.

Use la [**función MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para crear una lista de origen para una revisión que aún no se haya aplicado a ninguna aplicación en el contexto especificado. Esto puede ser útil al registrar una revisión para tener privilegios elevados. Para obtener más información sobre cómo registrar privilegios elevados para una revisión, vea Aplicación de [revisiones Per-User aplicaciones administradas.](patching-per-user-managed-applications.md)

Use la [**función MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) para quitar un origen existente para una aplicación o revisión en un contexto especificado. Quitar el origen actual de una aplicación o revisión obliga al instalador a buscar un origen en la lista de origen la próxima vez que se requiera un origen.

Use la [**función MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) para enumerar los orígenes en la lista de origen de una aplicación o revisión especificadas.

## <a name="managing-media-sources-for-products-and-patches"></a>Administración de orígenes multimedia para productos y revisiones

Use la [**función MsiSourceListAddMediaDisk para**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) agregar o actualizar la información de disco del origen multimedia de una aplicación o revisión registrada. Cada entrada se identifica de forma única mediante un identificador de disco. Si el disco ya existe, se actualiza con la nueva etiqueta de volumen y los valores del símbolo del sistema del disco. Si el disco no existe, se crea una nueva entrada de disco con los nuevos valores.

Use la [**función MsiSourceListClearMediaDisk para**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) quitar un disco registrado existente en el origen multimedia de una aplicación o revisión en un contexto específico.

Use la [**función MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) para enumerar una lista de discos registrados en el origen multimedia de una aplicación o revisión.

## <a name="retrieval-and-modification-of-source-list-information"></a>Recuperación y modificación de la información de la lista de origen

Use las [**funciones MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) y [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) para recuperar o modificar información sobre la lista de origen de una aplicación o revisión en un contexto específico. Use el *parámetro dwContext* para especificar el contexto de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario.

Se puede acceder a las propiedades de la lista de origen, como [**MEDIAPACKAGEPATH,**](mediapackagepath.md) [**DiskPrompt,**](diskprompt.md) **LastUsedSource,** **LastUsedType** y **PackageName.**

> [!Note]  
> La **propiedad de lista de origen LastUsedType** solo se puede leer. No se puede establecer directamente mediante [**la función MsiSourceListSetInfo.**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Borrar la lista de origen completa o forzar una resolución de origen

Use la [**función MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) para quitar todos los orígenes existentes de un tipo de origen determinado para la aplicación o instancia de revisión especificadas. El registro de revisiones también se quita si la revisión no está instalada por ninguna aplicación en el mismo contexto. Use el *parámetro dwContext* para especificar el contexto de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario.

Use [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) para borrar la última entrada de origen usada para una aplicación o revisión en el contexto especificado. Esta función quita el registro de la propiedad denominada **LastUsedSource.** Esta función no afecta a la lista de orígenes registrados. Borrar el **registro LastUsedSource** obliga al instalador a realizar una resolución de origen en los orígenes registrados la próxima vez que requiera el origen.

 

 



