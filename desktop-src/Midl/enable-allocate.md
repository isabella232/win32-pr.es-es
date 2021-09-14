---
title: enable_allocate atributo
description: El atributo \ enable allocate\ ACF especifica que el código auxiliar del servidor \_ debe habilitar el entorno de administración de memoria de código auxiliar.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate atributo MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159607"
---
# <a name="enable_allocate-attribute"></a>atributo \_ enable allocate

El **\[ atributo enable \_ allocate \]** ACF especifica que el código auxiliar del servidor debe habilitar el entorno de administración de memoria de código auxiliar.

> [!Note]  
> El **\[ atributo enable \_ allocate \]** está obsoleto y ya no se admite.

 

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

*optional-attribute-list* 
</dt> <dd>

Especifica una lista de cero o más atributos MIDL adicionales.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz a la que se aplicará el atributo **\[ \_ enable allcoate. \]**

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el modo predeterminado, el código auxiliar del servidor habilita el entorno de memoria solo cuando se usa el atributo **\[ \_ enable \]** allocate. El entorno de administración de memoria debe estar habilitado para poder asignar memoria mediante [**RpcSmAllocate.**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate) En **el modo osf** (cuando se compila mediante el modificador [**/osf),**](-osf.md) el código auxiliar habilita este entorno automáticamente, o a petición cuando se usa el atributo **\[ \_ \] enable** allocate.

El código auxiliar del lado cliente puede ser sensible al entorno de administración de memoria de **Rpcss.** Si se ejecuta un código auxiliar de cliente confidencial cuando el paquete **Rpcss** está deshabilitado, se llama a los asignadores o desasignadores de usuario predeterminados (por ejemplo, [midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)). Cuando se habilita, **el paquete Rpcss** usa el par de asignador y desasignador del paquete. En el modo predeterminado, el cliente solo es confidencial cuando se usa el atributo **\[ \_ enable \]** allocate. Normalmente, el código auxiliar del lado cliente funciona en el entorno deshabilitado. En **el modo osf** (al compilar con el modificador [**/osf),**](-osf.md) el cliente siempre es sensible al entorno de administración de memoria **rpcss** y, por lo tanto, el atributo **\[ enable \_ allocate \]** no afectará a los códigos auxiliares del cliente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 