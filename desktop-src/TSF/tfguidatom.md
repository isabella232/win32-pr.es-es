---
title: TfGuidAtom (Msctf.h)
description: El tipo de datos TfGuidAtom identifica un GUID dentro de TSF. Para obtener un TfGuidAtom, se llama a ITfCategoryMgr RegisterGUID.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068803"
---
# <a name="tfguidatom"></a>TfGuidAtom

El **tipo de datos TfGuidAtom** identifica un **GUID** dentro de TSF. Para **obtener un tfguidAtom,** se llama a [**ITfCategoryMgr::RegisterGUID.**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a>Observaciones

Un **valor TfGuidAtom** solo es válido dentro del proceso desde el que se llama a **ITfCategoryMgr::RegisterGUID.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITfCategoryMgr::GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[**ITfCategoryMgr::IsEqualTfGuidAtom**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





