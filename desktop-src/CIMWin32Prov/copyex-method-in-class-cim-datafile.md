---
description: El método CopyEx copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Método CopyEx de la CIM_DataFile de datos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60d2d0e6802aac62384a9d686831867d556cdb2c4a63630199c9989a5263188a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547485"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a>Método CopyEx de la clase \_ DataFile de CIM

El **método CopyEx** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el *parámetro FileName.* No se admite una copia si requiere sobrescribir un archivo lógico existente. Este método es una versión extendida del [**método Copy**](copy-method-in-class-cim-datafile.md) y se hereda de [CIM \_ LogicalFile](cim-logicalfile.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* \[ En\]
</dt> <dd>

Nombre completo del archivo de destino (o directorio).

Ejemplo: "c: \\ temp \\ newdirectory"

</dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadena que representa el nombre del archivo (o directorio) en el que se ha fallado el método. Este parámetro será **NULL si** el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ En\]
</dt> <dd>

Cadena que representa el archivo secundario (o directorio) que se va a usar como punto de partida para este método. Normalmente, el *parámetro StartFileName* es el *parámetro StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null,** la operación se realiza en el archivo (o directorio) especificado en la [**llamada a ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

Si *se usa StartFileName,* *Recursive* también debe establecerse en true.

</dd> <dt>

*Recursiva* \[ En\]
</dt> <dd>

Si es TRUE, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la [**instancia \_ de DataFile de CIM.**](cim-datafile.md) En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>


</dt> <dd>

0

Correcto.

</dd> <dt>


</dt> <dd>

2

Acceso denegado:

</dd> <dt>


</dt> <dd>

8

Error no especificado.

</dd> <dt>


</dt> <dd>

9

Objeto no válido.

</dd> <dt>


</dt> <dd>

10

El objeto ya existe.

</dd> <dt>


</dt> <dd>

11

Sistema de archivos no NTFS.

</dd> <dt>


</dt> <dd>

12

Plataforma no Windows.

</dd> <dt>


</dt> <dd>

13

La unidad no es la misma.

</dd> <dt>


</dt> <dd>

14

El directorio no está vacío.

</dd> <dt>


</dt> <dd>

15

Infracción de uso compartido.

</dd> <dt>


</dt> <dd>

16

Archivo de inicio no válido.

</dd> <dt>


</dt> <dd>

17

Privilegio no mantenido.

</dd> <dt>


</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI implementa el método **CopyEx** [**en CIM \_ DataFile.**](cim-datafile.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Archivo de datos CIM \_**](cim-datafile.md)
</dt> <dt>

[Tareas wmi: archivos y carpetas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

