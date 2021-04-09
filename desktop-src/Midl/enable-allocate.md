---
title: enable_allocate atributo)
description: El atributo \ enable \_ allocate especifica que el código auxiliar del servidor debe habilitar el entorno de administración de memoria de código auxiliar.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate el atributo MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149206"
---
# <a name="enable_allocate-attribute"></a>habilitar \_ asignar atributo

El atributo **\[ habilitar \_ asignar \]** ACF especifica que el código auxiliar de servidor debe habilitar el entorno de administración de memoria de código auxiliar.

> [!Note]  
> El atributo **\[ enable \_ allocate \]** está obsoleto y ya no se admite.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica una lista de cero o más atributos MIDL adicionales.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

El nombre de la interfaz a la que se aplicará el atributo **\[ enable \_ allcoate \]** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el modo predeterminado, el código auxiliar de servidor habilita el entorno de memoria solo cuando se usa el atributo **\[ enable \_ allocate \]** . El entorno de administración de memoria debe estar habilitado para poder asignar memoria mediante [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate). En el modo de **OSF** (al compilar mediante el modificador [**/OSF**](-osf.md) ), el código auxiliar habilita este entorno automáticamente, o bien, si se solicita, se usa el atributo **\[ habilitar \_ asignación \]** .

El código auxiliar del lado cliente puede ser sensible al entorno de administración de memoria **RPCSS** . Si se ejecuta un código auxiliar de cliente confidencial cuando se deshabilita el paquete **RPCSS** , se llama al asignador o desasignadores de usuario predeterminado (por ejemplo, el [usuario de MIDL \_ \_ asigna](/windows/desktop/Rpc/the-midl-user-allocate-function)el /  [usuario de MIDL \_ \_ gratis](/windows/desktop/Rpc/the-midl-user-free-function)). Cuando está habilitado, el paquete **RPCSS** usa el par allocator/desasignador del paquete. En el modo predeterminado, el cliente es sensible solo cuando se usa el atributo **\[ enable \_ allocate \]** . Normalmente, el código auxiliar del lado cliente funciona en el entorno deshabilitado. En el modo de **OSF** (al compilar mediante el modificador [**/OSF**](-osf.md) ), el cliente siempre es sensible al entorno de administración de memoria **RPCSS** y, por lo tanto, el atributo **\[ enable \_ allocate \]** no afectará al código auxiliar del cliente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[\_asignación de usuarios de MIDL \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[usuario de MIDL \_ \_ gratis](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 