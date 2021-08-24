---
title: Interfaz IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Use la interfaz IEnumBackgroundCopyFiles para enumerar los archivos que contiene un trabajo. Para obtener un puntero de interfaz IEnumBackgroundCopyFiles, llame al método IBackgroundCopyJob EnumFiles.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- IEnumBackgroundCopyFiles (interfaz)
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
ms.openlocfilehash: c6cf97975d583a99145e32482bc097ebd6ce3cc052e62560a34f7f78c1f88ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635685"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>IEnumBackgroundCopyFiles (interfaz)

Use la **interfaz IEnumBackgroundCopyFiles** para enumerar los archivos que contiene un trabajo. Para obtener un **puntero de interfaz IEnumBackgroundCopyFiles,** llame al [**método IBackgroundCopyJob::EnumFiles.**](ibackgroundcopyjob-enumfiles.md)

## <a name="members"></a>Miembros

La **interfaz IEnumBackgroundCopyFiles** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumBackgroundCopyFiles** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumBackgroundCopyFiles** tiene estos métodos.



| Método                                                | Descripción                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Recupera el número de elementos de la enumeración .<br/>                  |
| [**Next**](ienumbackgroundcopyfiles-next.md)         | Recupera un número especificado de elementos en la secuencia de enumeración.<br/> |
| [**Restablecer**](ienumbackgroundcopyfiles-reset.md)       | Restablece la secuencia de enumeración al principio.<br/>                  |
| [**Omitir**](ienumbackgroundcopyfiles-skip.md)         | Omite un número especificado de elementos en la secuencia de enumeración.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

