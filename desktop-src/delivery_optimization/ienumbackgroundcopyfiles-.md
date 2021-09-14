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
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963995"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>IEnumBackgroundCopyFiles (interfaz)

Use la **interfaz IEnumBackgroundCopyFiles** para enumerar los archivos que contiene un trabajo. Para obtener un **puntero de interfaz IEnumBackgroundCopyFiles,** llame al [**método IBackgroundCopyJob::EnumFiles.**](ibackgroundcopyjob-enumfiles.md)

## <a name="members"></a>Members

La **interfaz IEnumBackgroundCopyFiles** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumBackgroundCopyFiles** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumBackgroundCopyFiles** tiene estos métodos.



| Método                                                | Descripción                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Recupera el número de elementos de la enumeración .<br/>                  |
| [**Next**](ienumbackgroundcopyfiles-next.md)         | Recupera un número especificado de elementos en la secuencia de enumeración.<br/> |
| [**Reset**](ienumbackgroundcopyfiles-reset.md)       | Restablece la secuencia de enumeración al principio.<br/>                  |
| [**Saltar**](ienumbackgroundcopyfiles-skip.md)         | Omite un número especificado de elementos en la secuencia de enumeración.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

