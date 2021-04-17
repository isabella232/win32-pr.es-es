---
description: En ocasiones, es posible que necesite instalar una versión más reciente de un proveedor en un sistema en ejecución.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Actualizar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697414"
---
# <a name="updating-a-provider"></a>Actualizar un proveedor

En ocasiones, es posible que necesite instalar una versión más reciente de un proveedor en un sistema en ejecución. Si el proveedor está instalado como un archivo DLL, puede instalar un nuevo proveedor sin tener que reiniciar el servicio, reiniciar el equipo o afectar de algún modo a las aplicaciones que usan WMI en ese momento.

En el procedimiento siguiente se describe cómo actualizar un proveedor.

**Para actualizar un proveedor**

1.  Cree el nuevo proveedor.

    1.  Compile el nuevo proveedor con un nombre de archivo DLL diferente y un **CLSID** diferente.

        Por ejemplo, cambie Myprov.dll a Myprov1.dll y **CLSID \_ MyProProv** a **CLSID \_ MyProv** 1.

    2.  Modifique el archivo MOF de registro del proveedor para usar el nuevo CLSID (CLSID \_ MyProv1), pero el mismo nombre de proveedor ("MyProv").

2.  Instale el nuevo proveedor.

    1.  Copie el nuevo archivo DLL de proveedor con el nuevo nombre junto con el anterior.
    2.  Registre automáticamente el nuevo proveedor.

        Por ejemplo, use el comando **regsvr32** **myprov1.dll** para registrar el nuevo proveedor.

    3.  Compile el nuevo registro del proveedor MOF, con lo que se sobrescribirá el registro del proveedor anterior. Hasta este punto, el proveedor anterior era totalmente funcional. ahora el nuevo proveedor está totalmente operativo.

3.  Quite la versión anterior del proveedor, si es necesario.

    1.  Anule el registro del archivo DLL antiguo.

        Por ejemplo, use el comando **regsvr32** **/umyprov.dll** para anular el registro del archivo dll antiguo.

    2.  Marque el archivo DLL anterior que se eliminará al reiniciar llamando a [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).

Puede realizar pasos similares para actualizar un proveedor implementado en el servidor local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 
