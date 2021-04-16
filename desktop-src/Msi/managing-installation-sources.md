---
description: Los usuarios y las aplicaciones con privilegios administrativos pueden recuperar y modificar la información de la lista de origen de la red, la dirección URL y el medio para Windows Installer Aplicaciones y revisiones del sistema.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Administrar orígenes de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fc45253af20ae5f9792ee3a5ec7dd318c80295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678401"
---
# <a name="managing-installation-sources"></a>Administrar orígenes de instalación

Los usuarios y las aplicaciones con privilegios administrativos pueden recuperar y modificar la información de la lista de origen de la red, la dirección URL y el medio para Windows Installer Aplicaciones y revisiones del sistema.

**Windows Installer 2,0:** No compatible. Los administradores no pueden leer, reordenar o reemplazar entradas en la lista de origen y no pueden modificar ni recuperar las propiedades de la lista de origen. Es posible administrar los orígenes de red, pero no los orígenes de la dirección URL o los medios. Los administradores solo pueden administrar listas de origen para aplicaciones por equipo o aplicaciones instaladas por usuario para el usuario actual. Esto impide que los administradores con versiones anteriores a Windows Installer versión 3,0 de administren la información de la lista de origen de todos los usuarios del sistema.

**Windows Installer 3,0 y versiones posteriores:** Los usuarios y las aplicaciones que tienen privilegios de administrador pueden recuperar y modificar la información de la lista de origen de Windows Installer Aplicaciones y revisiones instaladas en el sistema para todos los usuarios. Las funciones de lista de origen se pueden usar para administrar las listas de origen y las propiedades de la lista de origen de los orígenes de red, URL y multimedia. El instalador puede reordenar las listas de origen desde un proceso externo.

Los usuarios y las aplicaciones que tienen privilegios administrativos pueden leer y modificar los siguientes tipos de información de lista de origen:

-   Listas de origen para aplicaciones y revisiones instaladas para todos los usuarios del sistema.
-   Listas de origen para los orígenes de revisiones que se encuentran aparte de los orígenes de la aplicación.
-   Listas de origen para orígenes de direcciones URL y multimedia que existen aparte de los orígenes de red.
-   Propiedades de la lista de origen como [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** y **packagename**.

Las funciones de listas de origen pueden limitar el ámbito de las listas de origen que se encuentran al especificar el contexto de instalación y el contexto de usuario. Hay tres contextos de instalación posibles: por usuario (no administrado), por equipo y por usuario administrado. El contexto de usuario puede ser un usuario determinado o todos los usuarios del sistema.

Los usuarios que no son administradores no pueden modificar la lista de origen de una instancia de una aplicación o revisión que existe en el contexto por usuario (administrado o no administrado) de otro usuario. Los usuarios que no son administradores pueden modificar las listas de origen de una instancia de una aplicación o revisión instalada en los contextos siguientes:

-   Su propio contexto por usuario (no administrado).
-   El contexto de la máquina, pero solo si las directivas [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)y [AlwaysInstallElevated](alwaysinstallelevated.md) le permiten buscar una aplicación o un origen de revisión.
-   Su propio contexto administrado por usuario, pero solo si las directivas [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)y [AlwaysInstallElevated](alwaysinstallelevated.md) le permiten buscar una aplicación o un origen de revisión.

Los administradores pueden modificar cualquier lista de origen que un usuario no administrador pueda modificar. Además, los administradores y las aplicaciones que tienen privilegios administrativos pueden modificar las listas de origen de una aplicación o revisión instalada en los contextos siguientes:

-   Contexto por máquina.
-   Sus propios usuarios (no administrados) o su propio contexto administrado por usuario.
-   Contexto administrado por usuario de otro usuario.

> [!Note]  
> Los usuarios y las aplicaciones que tienen privilegios administrativos no pueden modificar la lista de origen de una instancia de una aplicación o revisión instalada en el contexto por usuario (no administrado) de otro usuario.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Administración de orígenes de red y URL para productos y revisiones

Use la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para agregar o cambiar el orden de la lista de origen de los orígenes de red y URL para una revisión o aplicación en un contexto determinado. Use el parámetro *dwContext* para especificar el contexto de instalación. Use el parámetro *szUserSid* para especificar el contexto de usuario.

Utilice la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para crear una lista de origen para una revisión que no se haya aplicado todavía a ninguna aplicación en el contexto especificado. Esto puede ser útil cuando se registra una revisión para tener privilegios elevados. Para obtener más información acerca del registro de privilegios elevados para una revisión, consulte [aplicación de revisiones Per-User aplicaciones administradas](patching-per-user-managed-applications.md).

Utilice la función [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) para quitar un origen existente para una aplicación o revisión en un contexto especificado. Quitar el origen actual de una aplicación o revisión obliga al instalador a buscar un origen en la lista de origen la próxima vez que se requiera un origen.

Utilice la función [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) para enumerar los orígenes de la lista de origen de una revisión o aplicación especificada.

## <a name="managing-media-sources-for-products-and-patches"></a>Administración de orígenes de medios para productos y revisiones

Utilice la función [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) para agregar o actualizar la información de disco del origen multimedia de una aplicación o revisión registrada. Cada entrada se identifica de forma única mediante un identificador de disco. Si el disco ya existe, se actualiza con la nueva etiqueta de volumen y los valores de petición de disco. Si el disco no existe, se crea una nueva entrada de disco con los nuevos valores.

Utilice la función [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) para quitar un disco registrado existente en el origen de medios para una aplicación o revisión en un contexto específico.

Utilice la función [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) para enumerar una lista de discos registrados en el origen de medios para una aplicación o revisión.

## <a name="retrieval-and-modification-of-source-list-information"></a>Recuperación y modificación de la información de la lista de origen

Use las funciones [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) y [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) para recuperar o modificar la información sobre la lista de origen de una aplicación o revisión en un contexto específico. Use el parámetro *dwContext* para especificar el contexto de instalación. Use el parámetro *szUserSid* para especificar el contexto de usuario.

Se puede tener acceso a las propiedades de la lista de origen como [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** y **packagename** .

> [!Note]  
> Solo se puede leer la propiedad de lista de origen de **LastUsedType** . No se puede establecer directamente mediante la función [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) .

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Borrar la lista de origen completa o forzar una resolución de origen

Utilice la función [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) para quitar todos los orígenes existentes de un tipo de origen determinado para la aplicación o instancia de revisión especificada. También se quita el registro de revisiones si ninguna aplicación del mismo contexto instala la revisión. Use el parámetro *dwContext* para especificar el contexto de instalación. Use el parámetro *szUserSid* para especificar el contexto de usuario.

Use [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) para borrar la última entrada de origen usada para una aplicación o revisión en el contexto especificado. Esta función quita el registro de la propiedad denominada **LastUsedSource**. Esta función no afecta a la lista de orígenes registrados. Al borrar el registro de **LastUsedSource** , el instalador realiza una resolución de origen en los orígenes registrados la próxima vez que requiera el origen.

 

 



