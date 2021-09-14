---
description: A veces es posible que tenga que instalar una versión más reciente de un proveedor en un sistema en ejecución.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Actualizar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241646"
---
# <a name="updating-a-provider"></a>Actualizar un proveedor

A veces es posible que tenga que instalar una versión más reciente de un proveedor en un sistema en ejecución. Si el proveedor se instala como un archivo DLL, puede instalar un nuevo proveedor sin tener que reiniciar el servicio, reiniciar el equipo o afectar de otro modo a las aplicaciones que usan WMI en ese momento.

En el procedimiento siguiente se describe cómo actualizar un proveedor.

**Para actualizar un proveedor**

1.  Compile el nuevo proveedor.

    1.  Compile el nuevo proveedor con un nombre dll diferente y un **CLSID diferente.**

        Por ejemplo, cambie Myprov.dll a Myprov1.dll y **CLSID \_ MyProProv** a **CLSID \_ MyProv** 1.

    2.  Modifique el archivo MOF de registro del proveedor para usar el nuevo CLSID (CLSID MyProv1), pero el mismo nombre de \_ proveedor ("MyProv").

2.  Instale el nuevo proveedor.

    1.  Copie el nuevo archivo DLL del proveedor con el nuevo nombre junto con el antiguo.
    2.  Registre el nuevo proveedor de forma independiente.

        Por ejemplo, use el **comando regsvr32** **myprov1.dll** para registrar el nuevo proveedor.

    3.  Compile el nuevo MOF de registro de proveedor, sobrescribiendo así el registro de proveedor anterior. Hasta este momento, el proveedor antiguo era totalmente funcional; ahora el nuevo proveedor está totalmente operativo.

3.  Quite la versión anterior del proveedor, si es necesario.

    1.  Anula el registro del archivo DLL antiguo.

        Por ejemplo, use el **comando regsvr32** **/umyprov.dll** para anular el registro del archivo DLL anterior.

    2.  Marque el archivo DLL antiguo que se va a eliminar al reiniciar llamando a [**MoveFileEx.**](/windows/desktop/api/winbase/nf-winbase-movefileexa)

Puede realizar pasos similares para actualizar un proveedor local implementado por el servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Establecer descriptores de seguridad de namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 
