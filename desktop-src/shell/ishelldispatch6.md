---
description: Extiende el objeto IShellDispatch5.
title: Objeto IShellDispatch6 (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: 42e9690ec5b2f5995b184e4e686b27037aab891d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154933"
---
# <a name="ishelldispatch6-object"></a>Objeto IShellDispatch6

Extiende el objeto [**IShellDispatch5**](ishelldispatch5.md) . Además de las propiedades y los métodos admitidos por **IShellDispatch5**, **IShellDispatch6** agrega un método que muestra el panel de búsqueda de aplicaciones.

> [!Note]  
> **IShellDispatch6** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .

 

## <a name="members"></a>Miembros

El objeto **IShellDispatch6** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **IShellDispatch6** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**SearchCommand**](ishelldispatch6-searchcommand.md) | Muestra el panel de búsqueda de aplicaciones, que normalmente aparece cuando empieza a escribir un término de búsqueda en la pantalla Inicio.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto de Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> <dt>

[**IShellDispatch4**](ishelldispatch4.md)
</dt> <dt>

[**IShellDispatch5**](ishelldispatch5.md)
</dt> </dl>

 

 
