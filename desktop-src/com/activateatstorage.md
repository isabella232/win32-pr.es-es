---
title: ActivateAtStorage
description: Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que usan o desde el que se inicializan.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valor del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369540"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que usan o desde el que se inicializan.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg.** Cualquier valor que comience por "Y" o "y" indica que se debe usar **ActivateAtStorage.**

La **funcionalidad ActivateAtStorage** proporciona una manera transparente de permitir que los clientes busquen objetos en ejecución en el mismo equipo que los datos que usan. Esto reduce el tráfico de red porque el objeto realiza llamadas del sistema de archivos local en lugar de llamadas a través de la red.

Cuando se establece un valor para **ActivateAtStorage**, se convierte en el comportamiento predeterminado en las llamadas a las funciones [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) y [**CoGetInstanceFromIStorage,**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) así como a la implementación del moniker de archivo [**de IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). En todas estas llamadas, la especificación de una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) invalida la configuración **de ActivateAtStorage** mientras dure la llamada de función. El autor de la llamada puede pasar información **de COSERVERINFO** **a IMoniker::BindToObject a** través de la estructura BIND [**\_ OPTS2.**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)

El valor establecido para **ActivateAtStorage** también es el comportamiento predeterminado cuando se especifica CLSCTX REMOTE SERVER si no hay ninguna información del Registro para la clase instalada en el \_ equipo del \_ cliente. Por lo tanto, las aplicaciones cliente escritas para aprovechar **ActivateAtStorage** pueden requerir menos administración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> </dl>

 

 