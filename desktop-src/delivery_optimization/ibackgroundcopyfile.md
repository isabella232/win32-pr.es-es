---
title: Interfaz IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contiene información acerca de un archivo que forma parte de un trabajo. Por ejemplo, puede usar métodos IBackgroundCopyFile para recuperar los nombres locales y remotos del archivo y transferir la información de progreso.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705133"
---
# <a name="ibackgroundcopyfile-interface"></a>Interfaz IBackgroundCopyFile

**IBackgroundCopyFile** contiene información acerca de un archivo que forma parte de un trabajo. Por ejemplo, puede usar métodos **IBackgroundCopyFile** para recuperar los nombres locales y remotos del archivo y transferir la información de progreso.

Para obtener un puntero de interfaz **IBackgroundCopyFile** , llame al método [**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md) o al método [**IEnumBackgroundCopyFiles:: Next**](ienumbackgroundcopyfiles-next.md) .

## <a name="members"></a>Miembros

La interfaz **IBackgroundCopyFile** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBackgroundCopyFile** tiene estos métodos.



| Método                                                            | Descripción                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)   | Recupera el nombre local del archivo.<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | Recupera el progreso de la transferencia de archivos.<br/> |
| [**GetRemoteName**](ibackgroundcopyfile-getremotename-method.md) | Recupera el nombre remoto del archivo.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

