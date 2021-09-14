---
description: Este documento contiene una lista de los códigos de error definidos Windows Imaging Component (WIC).
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: Códigos de error de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd502ca1866114e2b471059bc9d9af1b0f96309f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362795"
---
# <a name="codec-error-codes"></a>Códigos de error de códec

Este documento contiene una lista de los códigos de error definidos Windows Imaging Component (WIC).

-   [Errores de WIC por código](#wic-errors-by-code)
-   [Errores de WIC por valor](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>Errores de WIC por código

La tabla siguiente es una lista de los códigos de error usados por los WICAPIs ordenados en orden alfabético. 

| Código de error                                      | Valor de error                      |
|-------------------------------------------------|----------------------------------|
| ERROR DE WINCODEC \_ \_ ANULADO                          | 0x80004004 (E \_ ABORT)            |
| ACCESO DE \_ ERROR DE WINCODECDENIED \_                     | 0x80070005 (E \_ ACCESSDENIED)     |
| ERROR DE WINCODEC \_ \_ YA CON BLOQUEO                    | 0x88982f0D                       |
| ERROR \_ BADHEADER de WINCODEC \_                        | 0x88982f61                       |
| ERROR \_ BADIMAGE de WINCODEC \_                         | 0x88982f60                       |
| ERROR DE WINCODEC \_ \_ BADMETADATAHEADER                | 0x88982f63                       |
| ERROR DE WINCODEC \_ \_ BADSTREAMDATA                    | 0x88982f70                       |
| CÓDEC DE \_ ERROR DE WINCODECNOTHUMBNAIL \_                 | 0x88982f44                       |
| CÓDECPRESENT \_ DE ERROR DE WINCODEC \_                     | 0x88982f43                       |
| CÓDEC DE \_ ERROR DE WINCODECTOOMANYSCANLINES \_            | 0x88982f46                       |
| COMPONENTE DE \_ ERROR DE WINCODECINITIALIZEFAILURE \_       | 0x88982f8B                       |
| COMPONENTE DE \_ ERROR DE WINCODECNOTFOUND \_                | 0x88982f50                       |
| ERROR DE WINCODEC \_ \_ DUPLICATEMETADATAPRESENT         | 0x88982f8D                       |
| ERROR DE WINCODEC \_ \_ FRAMEMISSING                     | 0x88982f62                       |
| ERROR GENÉRICO DE ERROR GENÉRICO \_ DE ERROR \_ DE WINCODEC \_                   | 0x80004005 (E \_ FAIL)             |
| IMÁGENES DE \_ ERROR DE WINCODECIZEOUTOFRANGE \_              | 0x88982f51                       |
| ERROR DE WINCODEC \_ \_ INSUFFICIENTBUFFER               | 0x88982f8C                       |
| ERROR \_ INTERNALERROR DE WINCODEC \_                    | 0x88982f48                       |
| ERROR DE WINCODEC \_ \_ INVALIDPARAMETER                 | 0x80070057 (E \_ INVALIDARG)       |
| ERROR DE WINCODEC \_ \_ INVALIDQUERYCHARACTER            | 0x88982f93                       |
| ERROR DE WINCODEC \_ \_ INVALIDQUERYREQUEST              | 0x88982f90                       |
| ERROR DE WINCODEC \_ \_ INVALIDREGISTRATION              | 0x88982f8A                       |
| ERROR DE WINCODEC \_ \_ NOTIMPLEMENTED                   | 0x80004001 (E \_ NOTIMPL)          |
| ERROR DE WINCODEC \_ \_ NOTINITIALIZED                   | 0x88982f0C                       |
| ERROR DE WINCODEC \_ \_ OUTOFMEMORY                      | 0x8007000E (E \_ OUTOFMEMORY)      |
| PALETA DE \_ ERRORES DE WINCODECUNAVAILABLE \_               | 0x88982f45                       |
| PROPIEDAD ERR \_ DE WINCODECNOTFOUND \_                 | 0x88982f40                       |
| PROPIEDAD \_ ERR DE WINCODECNOTSUPPORTED \_             | 0x88982f41                       |
| WINCODEC \_ ERR \_ PROPERTYSIZE                     | 0x88982f42                       |
| PROPIEDAD \_ ERR DE WINCODECUNEXPECTEDTYPE \_           | 0x88982f8E                       |
| WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   | 0x88982f92                       |
| WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS | 0x88982f49                       |
| WINCODEC \_ ERR \_ STREAMWRITE                      | 0x88982f71                       |
| WINCODEC \_ ERR \_ STREAMREAD                       | 0x88982f72                       |
| SECUENCIA DE ERROR DE WINCODECNO \_ \_ DISPONIBLE               | 0x88982f73                       |
| ERROR DE WINCODEC \_ \_ TOOMUCHMETADATA                  | 0x88982f52                       |
| ERROR DE WINCODEC \_ \_ UNKNOWNIMAGEFORMAT               | 0x88982f07                       |
| ERROR INESPERADO DE \_ WINCODECMETADATATYPE \_           | 0x88982f91                       |
| ERROR DE WINCODEC \_ \_ UNEXPECTEDSIZE                   | 0x88982f8F                       |
| ERROR DE WINCODEC \_ \_ UNSUPPORTEDOPERATION             | 0x88982f81                       |
| ERROR DE WINCODEC \_ \_ UNSUPPORTEDPIXELFORMAT           | 0x88982f80                       |
| ERROR DE WINCODEC \_ \_ UNSUPPORTEDVERSION               | 0x88982f0B                       |
| ERROR DE WINCODEC \_ \_ VALUEOUTOFRANGE                  | 0x88982f05                       |
| WINCODEC \_ ERR \_ VALUEOVERFLOW                    | DESBORDAMIENTO \_ \_ ARITMÉTICO INTSAFE E \_ |
| ERROR DE ERROR DE WINCODEC \_ \_                       | 0x88982f04                       |



 

## <a name="wic-errors-by-value"></a>Errores de WIC por valor

La tabla siguiente es una lista de los códigos de error usados por los WICAPIs ordenados en orden numérico. 

| Código de error                       | Valor de error                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_ FAIL)             | ERROR GENÉRICO DE ERROR GENÉRICO \_ DE ERROR \_ DE WINCODEC \_                   |
| 0x80070057 (E \_ INVALIDARG)       | ERROR DE WINCODEC \_ \_ INVALIDPARAMETER                 |
| 0x8007000E (E \_ OUTOFMEMORY)      | ERROR DE WINCODEC \_ \_ OUTOFMEMORY                      |
| 0x80004001 (E \_ NOTIMPL)          | ERROR DE WINCODEC \_ \_ NOTIMPLEMENTED                   |
| 0x80004004 (E \_ ABORT)            | ERROR DE WINCODEC \_ \_ ANULADO                          |
| 0x80070005 (E \_ ACCESSDENIED)     | ACCESO DE \_ ERROR DE WINCODECDENIED \_                     |
| DESBORDAMIENTO \_ \_ ARITMÉTICO INTSAFE E \_ | WINCODEC \_ ERR \_ VALUEOVERFLOW                    |
| 0x88982f04                       | ERROR DE WINCODEC \_ \_ WRONGSTATE                       |
| 0x88982f05                       | ERROR DE WINCODEC \_ \_ VALUEOUTOFRANGE                  |
| 0x88982f07                       | ERROR DE WINCODEC \_ \_ UNKNOWNIMAGEFORMAT               |
| 0x88982f0B                       | ERROR DE WINCODEC \_ \_ UNSUPPORTEDVERSION               |
| 0x88982f0C                       | ERROR DE WINCODEC \_ \_ NOTINITIALIZED                   |
| 0x88982f0D                       | ERROR DE WINCODEC \_ \_ ALREADYLOCKED                    |
| 0x88982f40                       | PROPIEDAD ERR \_ DE WINCODECNOTFOUND \_                 |
| 0x88982f41                       | PROPIEDAD \_ ERR DE WINCODECNOTSUPPORTED \_             |
| 0x88982f42                       | WINCODEC \_ ERR \_ PROPERTYSIZE                     |
| 0x88982f43                       | CODECPRESENT DE \_ ERROR DE WINCODEC \_                     |
| 0x88982f44                       | CÓDEC DE \_ ERROR DE WINCODECNOTHUMBNAIL \_                 |
| 0x88982f45                       | PALETA DE \_ ERRORES DE WINCODECUNAVAILABLE \_               |
| 0x88982f46                       | \_ \_ CÓDECTOOMANYSCANLINES DE ERROR DE WINCODEC            |
| 0x88982f48                       | ERROR \_ INTERNALERROR DE WINCODEC \_                    |
| 0x88982f49                       | WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS |
| 0x88982f50                       | COMPONENTE ERR \_ DE WINCODECNOTFOUND \_                |
| 0x88982f51                       | IMÁGENES DE \_ ERROR DE WINCODECIZEOUTOFRANGE \_              |
| 0x88982f52                       | ERROR DE WINCODEC \_ \_ TOOMUCHMETADATA                  |
| 0x88982f60                       | ERROR \_ BADIMAGE de WINCODEC \_                         |
| 0x88982f61                       | WINCODEC \_ ERR \_ BADHEADER                        |
| 0x88982f62                       | ERROR \_ \_ FRAMEMISSING DE WINCODEC                     |
| 0x88982f63                       | WINCODEC \_ ERR \_ BADMETADATAHEADER                |
| 0x88982f70                       | ERROR DE WINCODEC \_ \_ BADSTREAMDATA                    |
| 0x88982f71                       | WINCODEC \_ ERR \_ STREAMWRITE                      |
| 0x88982f72                       | WINCODEC \_ ERR \_ STREAMREAD                       |
| 0x88982f73                       | WINCODEC \_ ERR \_ STREAMNOTAVAILABLE               |
| 0x88982f80                       | ERROR DE WINCODEC \_ \_ UNSUPPORTEDPIXELFORMAT           |
| 0x88982f81                       | ERROR DE WINCODEC \_ \_ UNSUPPORTEDOPERATION             |
| 0x88982f8A                       | ERROR DE WINCODEC \_ \_ INVALIDREGISTRATION              |
| 0x88982f8B                       | COMPONENTE ERR \_ DE WINCODECINITIALIZEFAILURE \_       |
| 0x88982f8C                       | ERROR \_ INSUFFICIENTBUFFER de WINCODEC \_               |
| 0x88982f8D                       | ERROR DE WINCODEC \_ \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f8E                       | PROPIEDAD \_ ERR DE WINCODECUNEXPECTEDTYPE \_           |
| 0x88982f8F                       | ERROR DE WINCODEC \_ \_ UNEXPECTEDSIZE                   |
| 0x88982f90                       | ERROR DE WINCODEC \_ \_ INVALIDQUERYREQUEST              |
| 0x88982f91                       | ERROR INESPERADO \_ DE WINCODECMETADATATYPE \_           |
| 0x88982f92                       | WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982f93                       | ERROR DE WINCODEC \_ \_ INVALIDQUERYCHARACTER            |



 

 

 



