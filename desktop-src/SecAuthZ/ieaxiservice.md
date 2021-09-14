---
description: Inicializa un objeto de servicio del sistema para instalar un objeto ActiveX cuando el usuario actual no tiene permiso para instalar el objeto.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interfaz IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073689"
---
# <a name="ieaxiservice-interface"></a>Interfaz IeAxiService

La **interfaz IAxiService** inicializa un objeto de servicio del sistema para instalar un objeto ActiveX cuando el usuario actual no tiene permiso para instalar el objeto.

La [**clase CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa esta interfaz.

Esta interfaz no se declara en un encabezado público. Las aplicaciones deben definirla por sí mismas. El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe esta interfaz, incluido su IID.

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>Members

La **interfaz IeAxiService** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiService** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IeAxiService** tiene estos métodos.



| Método                                        | Descripción                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Limpieza**](ieaxiservice-cleanup.md)       | Libera los recursos usados por la **interfaz IeAxiService.**<br/> |
| [**Inicialización**](ieaxiservice-initialize.md) | Comprueba y descarga un ActiveX objeto .<br/>                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Business, Windows Vista Enterprise, Windows aplicaciones de escritorio de Vista \[ Ultimate\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService se define como E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 

