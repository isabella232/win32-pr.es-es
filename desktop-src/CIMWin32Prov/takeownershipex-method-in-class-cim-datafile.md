---
description: Obtiene la propiedad del archivo de datos lógicos que se especifica en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip y se hereda de CIM \_ LogicalFile.
ms.assetid: 3bc5a060-d805-46f6-802d-9ed16b52da59
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la CIM_DataFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41124567e8743227f46c9cb3b84dcb0d1f788bc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062258"
---
# <a name="takeownershipex-method-of-the-cim_datafile-class"></a>Método TakeOwnerShipEx de la clase \_ DataFile de CIM

El **método TakeOwnerShipEx** obtiene la propiedad del archivo de datos lógico que se especifica en la ruta de acceso del objeto. Este método es una versión extendida del [**método TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md). Si el archivo lógico es un directorio, este método actuará de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 TakeOwnerShipEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nombre del archivo (o directorio) en el que se ha fallado el método. Este parámetro será NULL si el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ En\]
</dt> <dd>

Archivo secundario (o directorio) que se va a usar como punto de partida para este método. Normalmente, el *parámetro StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior. Si este parámetro es NULL, la operación se realiza en el archivo (o directorio) especificado en la [**llamada a ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

Si *se usa StartFileName,* *Recursive* también debe establecerse en true.

</dd> <dt>

*Recursivo* \[ En\]
</dt> <dd>

Si **es TRUE,** el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia [**de \_ DataFile**](cim-datafile.md) de CIM. En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Correcto.

</dd> <dt>

**2**
</dt> <dd>

Acceso denegado.

</dd> <dt>

**8**
</dt> <dd>

Error no especificado.

</dd> <dt>

**9**
</dt> <dd>

Objeto no válido.

</dd> <dt>

**10**
</dt> <dd>

El objeto ya existe.

</dd> <dt>

**11**
</dt> <dd>

El sistema de archivos no es NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plataforma no Windows.

</dd> <dt>

**13**
</dt> <dd>

La unidad no es la misma.

</dd> <dt>

**14**
</dt> <dd>

El directorio no está vacío.

</dd> <dt>

**15**
</dt> <dd>

Infracción de uso compartido.

</dd> <dt>

**16**
</dt> <dd>

Archivo de inicio no válido.

</dd> <dt>

**17**
</dt> <dd>

Privilegios no mantenidos.

</dd> <dt>

**21**
</dt> <dd>

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI implementa el método **TakeOwnerShipEx** [**en CIM \_ DataFile.**](cim-datafile.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ DataFile](takeownershipex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Tareas wmi: archivos y carpetas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

