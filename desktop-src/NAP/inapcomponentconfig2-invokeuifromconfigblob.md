---
title: Método INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) según sea necesario para cargar la configuración de un equipo remoto o local en la memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Método InvokeUIFromConfigBlob NAP
- Método InvokeUIFromConfigBlob NAP, interfaz INapComponentConfig2
- Interfaz INapComponentConfig2 NAP, método InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905127"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>INapComponentConfig2:: InvokeUIFromConfigBlob (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de mantenimiento del sistema (SHV) implementan el método **InvokeUIFromConfigBlob** según sea necesario para cargar la configuración de un equipo remoto o local en la memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración. El componente de configuración debe admitir el uso de [**INapComponentConfig**](inapcomponentconfig.md) a través de DCOM.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Identificador de la ventana primaria o propietaria. Se debe proporcionar un identificador de ventana válido.

</dd> <dt>

*inbCount* \[ de\]
</dt> <dd>

Tamaño, en bytes, de los *datos*.

</dd> <dt>

*datos* \[ de de\]
</dt> <dd>

Puntero a un búfer que almacena los datos de configuración iniciales. Estos datos se exportan desde el equipo remoto o local.

</dd> <dt>

*outbCount* \[ enuncia\]
</dt> <dd>

Tamaño de los *datos*, en bytes.

</dd> <dt>

*outdata* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que almacena los datos de configuración modificados por la interfaz de usuario de la configuración de SHV. Estos datos son importados por el equipo remoto o local.

</dd> <dt>

*fConfigChanged* \[ enuncia\]
</dt> <dd>

Un puntero a un valor **booleano** que se establece en **true** si se cambió la configuración durante la operación de la interfaz de usuario y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o uno de los códigos de error estándar de Windows.

## <a name="remarks"></a>Observaciones

Si se usa para un equipo local, esta función se puede usar para la configuración de SHV por directiva. Proporciona una manera de invocar una interfaz de usuario de SHV y editar una configuración de SHV existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





