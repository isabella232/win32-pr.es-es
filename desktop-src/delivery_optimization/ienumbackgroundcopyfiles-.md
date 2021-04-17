---
title: Interfaz IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Use la interfaz IEnumBackgroundCopyFiles para enumerar los archivos que contiene un trabajo. Para obtener un puntero de interfaz IEnumBackgroundCopyFiles, llame al método IBackgroundCopyJob Enumfiles (.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, descrita
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714587"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Interfaz IEnumBackgroundCopyFiles

Use la interfaz **IEnumBackgroundCopyFiles** para enumerar los archivos que contiene un trabajo. Para obtener un puntero de interfaz **IEnumBackgroundCopyFiles** , llame al método [**IBackgroundCopyJob:: enumfiles (**](ibackgroundcopyjob-enumfiles.md) .

## <a name="members"></a>Miembros

La interfaz **IEnumBackgroundCopyFiles** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumBackgroundCopyFiles** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumBackgroundCopyFiles** tiene estos métodos.



| Método                                                | Descripción                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Recupera el número de elementos de la enumeración.<br/>                  |
| [**Next**](ienumbackgroundcopyfiles-next.md)         | Recupera un número especificado de elementos en la secuencia de enumeración.<br/> |
| [**Reset**](ienumbackgroundcopyfiles-reset.md)       | Restablece la secuencia de enumeración al principio.<br/>                  |
| [**Omitir**](ienumbackgroundcopyfiles-skip.md)         | Omite un número especificado de elementos en la secuencia de enumeración.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob:: Enumfiles (**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

