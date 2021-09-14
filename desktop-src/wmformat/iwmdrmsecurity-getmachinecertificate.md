---
title: Método IWMDRMSecurity GetMachineCertificate (Wmdrmsdk.h)
description: El método GetMachineCertificate recupera el certificado de máquina del subsistema DRM en el equipo cliente.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Método GetMachineCertificate windows Media Format
- Método GetMachineCertificate windows Media Format , interfaz IWMDRMSecurity
- IWMDRMSecurity interface windows Media Format , GetMachineCertificate method
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256263"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>IWMDRMSecurity::GetMachineCertificate (método)

El **método GetMachineCertificate** recupera el certificado de máquina del subsistema DRM en el equipo cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwCertificateType* \[ En\]
</dt> <dd>

Tipo de certificado que se recuperará. Establezca en uno de los valores de la tabla siguiente.



| Value                        | Descripción                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| TIPO DE CERTIFICADO WMDRM \_ \_ \_ V1 | El certificado se recuperará en el formato utilizado por los componentes heredados.            |
| TIPO DE CERTIFICADO WMDRM \_ \_ \_ V2 | El certificado se recuperará en el formato utilizado por los componentes Windows Vista. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[ out\]
</dt> <dd>

Matriz de cuatro bytes que especifica la versión del subsistema DRM en el equipo cliente.

</dd> <dt>

*ppbCertificate* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a los datos del certificado. Se establece **en NULL** para que el método proporcione el tamaño de búfer necesario para contener el certificado *encertificate.*

</dd> <dt>

*certificateCertificate* \[ in, out\]
</dt> <dd>

Tamaño del certificado en bytes. Si *ppbCertificate* es **NULL,** este valor se establecerá en el tamaño del certificado. Si *ppbCertificate* no es **NULL,** este valor debe establecerse en el tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMSecurity (interfaz)**](iwmdrmsecurity.md)
</dt> </dl>

 

 





