---
title: Método GetObjectDataOnClearChannel
description: El método GetObjectDataOnClearChannel transfiere un bloque de datos de objeto en un canal claro de vuelta a Windows Media Administrador de dispositivos.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Método GetObjectDataOnClearChannel windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10e09697653c2ef1235ae9a3ea3a93a45437d1cf45a1f4de72ec99b0812b9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619875"
---
# <a name="getobjectdataonclearchannel-method"></a>Método GetObjectDataOnClearChannel

El **método GetObjectDataOnClearChannel** transfiere un bloque de datos de objeto en un canal claro de vuelta a Windows Media Administrador de dispositivos.

Este método es idéntico a [**ISCPSecureExchange::ObjectData,**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) salvo que los datos devueltos por este método no están cifrados. Por lo tanto, este método es más eficaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* 
</dt> <dd>

Puntero al objeto de dispositivo.

</dd> <dt>

*pData* 
</dt> <dd>

Puntero a un búfer para recibir datos.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Puntero a un **DWORD** que contiene el tamaño de transferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error en el método , devuelve un código de error **HRESULT.**



| Código devuelto                                                                                                | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR DE COMPROBACIÓN DE \_ WMDM E \_ MAC \_ \_**</dt> </dl> | El código de autenticación del mensaje no es válido.<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ NORIGHTS**</dt> </dl>           | El autor de la llamada no tiene los derechos necesarios para realizar la operación solicitada.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Error en el método. Finalizar la interacción con el proveedor de contenido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Un parámetro es un puntero NULL **o no** válido.<br/>                                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Se ha producido un error no especificado.<br/>                                                   |



 

## <a name="remarks"></a>Comentarios

Para transferir datos, Windows Media Administrador de dispositivos llama al [método TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) para obtener los datos del contenedor. A continuación, se llama a **GetObjectDataOnClearChannel** para transferir bloques de datos de objeto desde el proveedor de contenido a Windows Media Administrador de dispositivos. Si se devuelve S \_ OK con *pdwSize* establecido en cero, Windows Media Administrador de dispositivos no solicitará más datos.

Este método es idéntico a [**ISCPSecureExchange::ObjectData,**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) salvo que los datos devueltos por este método no están cifrados. Por lo tanto, este método es más eficaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMSCP.idl</dt> </dl>    |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Interfaz ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





