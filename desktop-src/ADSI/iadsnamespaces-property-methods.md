---
title: Métodos de la propiedad IADsNamespaces (iAds. h)
description: Los métodos de propiedad de la interfaz IADsNamespaces obtienen y establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsNamespaces ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803170"
---
# <a name="iadsnamespaces-property-methods"></a>Métodos de propiedad IADsNamespaces

Los métodos de propiedad de la interfaz [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) obtienen y establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

La propiedad **DefaultContainer** identifica un objeto contenedor base al que se puede enlazar y utilizar como punto de partida al examinar. Estos datos se almacenan y recuperan del siguiente valor del registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI define la propiedad **DefaultContainer** para proporcionar una forma rápida de obtener un puntero a un objeto de contenedor ADSI definido previamente.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

Los proveedores deben proporcionar esta propiedad por usuario. El contenedor predeterminado se establece inmediatamente después de la invocación de **IADsNamespaces::p UT \_ DefaultContainer**. No es necesario llamar a [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . De hecho, el objeto de espacios de nombres proporcionado por el sistema devuelve **E \_ NOTIMPL** para el método **IADs. SetInfo** llamado en este objeto. Cuando un contenedor es el objeto namespaces, una operación de enumeración siempre da como resultado una lista de objetos de espacio de nombres específicos del proveedor. Cuando se usa [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) para obtener un objeto de espacio de nombres, se omite el parámetro *bstrClass* . Esto se debe a que el contenedor, es decir, el objeto namespaces, solo contiene un tipo de objeto, es decir, objetos de espacio de nombres específicos del proveedor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces se define como 28B96BA0-B330-11cf-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





