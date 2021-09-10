---
title: DllSurrogate
description: Permite que los servidores DLL se ejecuten en un proceso suplente. Si se especifica una cadena vacía, se usa el suplente proporcionado por el sistema; De lo contrario, el valor especifica la ruta de acceso del suplente que se va a usar.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- DllSurrogate registry value COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369708"
---
# <a name="dllsurrogate"></a>DllSurrogate

Permite que los servidores DLL se ejecuten en un proceso suplente. Si se especifica una cadena vacía, se usa el suplente proporcionado por el sistema; De lo contrario, el valor especifica la ruta de acceso del suplente que se va a usar.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg** que especifica que la clase es un archivo DLL que se va a activar en un proceso suplente y el proceso suplente que se va a usar. Para usar el proceso suplente genérico proporcionado por el sistema, establezca *path* en una cadena vacía o **NULL.** Para especificar otro proceso suplente, establezca *path* en la ruta de acceso del suplente. Como en la especificación de la ruta de acceso de un servidor bajo la clave [**LocalServer32,**](localserver32.md) no es necesaria una especificación de ruta de acceso completa. El suplente debe escribirse para comunicarse correctamente con el servicio DCOM, tal como se describe en [Writing a Custom Surrogate](writing-a-custom-surrogate.md).

El **valor DllSurrogate** debe estar presente para que un servidor DLL se active en un suplente. La activación hace referencia a una llamada a [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) [**CoCreateInstanceEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) **CoCreateInstanceEx,** [**CoGetInstanceFromFile,**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)o [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). La ejecución de archivos DLL en un proceso suplente proporciona las ventajas de una implementación ejecutable, incluido el aislamiento de errores, la capacidad de atender a varios clientes simultáneamente y permitir que el servidor proporcione servicios a clientes remotos en un entorno distribuido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Suplentes de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogateExecutable**](dllsurrogateexecutable.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 