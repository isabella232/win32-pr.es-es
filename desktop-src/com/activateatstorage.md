---
title: ActivateAtStorage
description: Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que están usando o desde el que se inicializan.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valor del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078458"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que están usando o desde el que se inicializan.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** . Cualquier valor que comience por ' Y ' o ' y ' indica que debe usarse **ActivateAtStorage** .

La funcionalidad **ActivateAtStorage** proporciona una manera transparente de permitir que los clientes busquen objetos en ejecución en el mismo equipo que los datos que usan. Esto reduce el tráfico de red porque el objeto realiza llamadas locales del sistema de archivos en lugar de llamadas a través de la red.

Cuando se establece un valor para **ActivateAtStorage**, este se convierte en el comportamiento predeterminado en las llamadas a las funciones [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) y [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , así como a la implementación del moniker de archivo de [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). En todas estas llamadas, si se especifica una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , se invalida el valor de **ActivateAtStorage** para la duración de la llamada de función. El autor de la llamada puede pasar información de **COSERVERINFO** a **IMoniker:: BindToObject** a través de la estructura [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .

El valor establecido para **ActivateAtStorage** también es el comportamiento predeterminado cuando \_ se especifica CLSCTX Remote \_ Server si no hay información del registro para la clase instalada en el equipo del cliente. Por tanto, las aplicaciones cliente escritas para aprovechar las ventajas de **ActivateAtStorage** pueden requerir menos administración.

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

[**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> </dl>

 

 